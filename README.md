# DC Comics

![Thumbail](/src/assets/readme-img/thumbnail.jpeg)

Creazione di una pagina web dopo aver introdotto 'npm' 'vite' 'vue' e 'scss'.

## Indice

- [Creazione e inizializzazione via Terminale](#creazione-e-inizializzazione-via-terminale)

- [Utilizzo dei components](#utilizzo-dei-components)

- [Svolgimento dell' esercizio](#svolgimento-dell-esercizio)
  - [Header](#appheader)
  - [Main](#appmain)
  - [Footer](#appfooter)

## Creazione e inizializzazione via Terminale

Tramite i comandi imparati a lezione si crea la cartella in cui inizializzare il progetto, di seguito i più utili:

- 'cd' per accedere alla cartella
- 'cd..' per tornare alla cartella precedente
- 'dir' per visualizzare i file nella cartella
- 'npm create vite@latest' per creare una cartella tramite vite

Dopo aver creato la cartella (seguendo le domande di vite) accedervi e avviare vsc (code .)

Dentro vsc avviare il terminale per poter installare i pacchetti relativi al progetto (npm install) e per avviare il server ('npm run dev')

In alternativa si può creare una repository template (già sistemata in base alle preferenze) su github da poter clonare dentro la cartella del nuovo progetto ('git clone url..')

Una volta creata la base andare a modificare la struttura di base in base alle preferenze (se non si è usato un template).

Per ora le 'regole' da seguire sono:

- mettere in public l' immagine logo che non si vuole comprimere
- mettere in assets le immagini, la cartella scss e la cartella js
- richiamare tutti i file '\_secondari' scss in main.scss
- richiamare il file main.scss nel file main.js
- avere file scss separati per le variabili e i mixin, unici file da richiamare nei components se necessario
- seguire una naming convenction per i components
  - AppHeader -> Header..
  - AppMain -> Main..
  - AppFooter -> Footer..
  - CommonElements

NB

Per intallare nuovi pacchetti eseguire il relativo comando nmp a server chiuso.

## Utilizzo dei components

Le regole imparate fino ad ora per continuano a essere valide ma necessitano di un cambio di prospettiva.

Tramite vite si ha la possibilità di scomporre il progetto in components, un processo che è sempre stato fatto a mente e che ora trova un riscontro pratico.

Le regole base per una corretta creazione e utilizzo di un compinent sono le seguenti:

- Un component contiente al suo interno html, css e js

```
<script>
JavaScript
</script>

<template>
HTML
</template>

<style>
CSS
</style>
```

- Per far si che un component possa richiamare o essere richiamato è necessario usare 'export default'

- Per richiamare un component si usa il comando import, si salva il component all' interno di components e lo si visualizza nell' html richiamandolo con una sintassi `<nome>`

```
Per richiamare un altro component
<script>
import AppFooter from "./components/AppFooter.vue";
export default {
components:{
    AppFooter,
}
}
</script>

<template>
  <AppFooter />
</template>

<style>
CSS
</style>
```

- All' interno di un component possiamo creare regole css uniche per l' elemento corrente (che si aggiungono a quelle globali date dal file importato in main.js)

```
<style scoped>

</style>
```

- Se si vuole utilizzare scss è necessario specificarlo

```
<style scoped lang="scss">

</style>
```

- Per comodità di può dare un nome al component

```
<script>
export default{
  name: "NomeComponents"
}
</script>
```

NB

In generale l' utilità dei components sta nella loro generalizzazione, creando components generali e indipendenti si possono riutilizzare più volte (nello stesso progetto o in un altro)

## Svolgimento dell' esercizio

Importo in App.vue i components AppHeader - AppMain - AppFooter

### AppHeader

Creo la struttura base dell' header e ci inserisco i relativi components

```
<script>
import HeaderLogo from "./HeaderLogo.vue";
import HeaderNav from "./HeaderNav.vue";

export default {
  name: "Header",
  components: {
    HeaderLogo,
    HeaderNav,
  },
};
</script>

<template>
  <header>
    <div class="container flex space-between align-center">
      <header-logo /> <header-nav />
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

header {
  height: $header-height;

  .container {
    @include container;  MIXIN
    height: 100%;
  }
}
</style>

```

Per il container ho utilizzato un @mixin di scss

```scss
@mixin container($width: 1280px) {
  width: $width;
  margin: 0 auto;
}
```

Questo mi permette di avere un container di default e, se necessario, dei container più grandi o più picolli a seconda della larghezza che passo alla funzione (come per js)

NB

Ho incluso nello stile il file scss variables perchè i @mixin e le $variables devono essere richiamati anche localmente

as \* alla fine del comando @use serve per poter richiamare la variabile senza specificare il file di provenienza (variables.$blue-primary)

I due componenti non presentano nessuna grossa novità tranne che per l' hover (con sass) e le immagini in public

```
in scss per dare un hover (o altro) all' elemento si richiama con &
 a {
     height: 100%;

      &:hover {
          border-bottom: 5px solid $blue-primary;
          border-top: 5px solid transparent;
          color: $blue-primary;
         }
   }
un immagine nella cartella public si richiama facilmente
<img src="/img/dc-logo.png" alt="Logo" />
```

### AppMain

Nel main richiamo semplicemente i componenti jumbotron e CurrentSeries (che conterrà la lista dei comics).

CommonSeries è un ottimo esempio di come un componente neutro si possa utilizzare per creare un componente molto più caratterizzato.

Infatti la struttura base (una semplice griglia) si andrà a popolare con un CommonElement (ripetuto con v-for)

```html
<template>
  <section class="current-series">
    <h2>Current Series</h2>
    <div class="container">
      <div class="comics flex">
        <CommonElement
          v-for="element in comics"
          :img="element.thumb"
          :text="element.series"
        />
      </div>
      <MainButton />
    </div>
  </section>
</template>

common element
<script>
  export default {
    props: {
      img: String,
      text: String,
    },
  };
</script>
<template>
  <div class="element">
    <div class="image">
      <img :src="img" :alt="text" />
    </div>
    <div class="text">{{ text }}</div>
  </div>
</template>
```

L' elemento base è un div che contiene un immagine e un testo (senza css) generico.

Tramite le 'props' passerò i dati necessari a riempire i vari elementi, che ripetendosi con un v-for creeranno una griglia composta dai singoli oggetti del mio array di partenza.

Come si vede nel codice le props vengono passate tramite v-bind

```
  <CommonElement
     v-for="element in comics"
    :img"element.thumb"
    :text="element.series"
   />

```

Vengono poi 'salvate' nel common element (specificandone il tipo)

```
  props: {
    img: String,
    text: String,
  },

```

E utilizzate per riempire l' elemento

```
  <div class="image">
    <img :src="img" :alt="text" />
  </div>
  <div class="text">{{ text }}</div>
```

Il css invece è presente nel componente padre e lo si passa al componente figlio (che così rimarrà generico) tramite 'deep'

```css
.container {
  @include container;
  height: 100%;

  .comics {
    flex-wrap: wrap;

    :deep(.element) {
      margin: 10px;
      text-transform: uppercase;
      text-align: start;
      width: calc(100% / 6 - 20px);

      .image {
        width: 100%;
        height: 250px;
        margin-bottom: 15px;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}
```

### AppFooter

Nel Footer si presenta solo una semplice applicazione del @mixin container per andare a creare un .container più piccolo del default

```css
section {
  background-color: $blue-primary;
  padding: 50px;
  .container {
    @include container(1200px);
  }
}
```

In questo caso specifico la larghezza desiderata (1200px)
