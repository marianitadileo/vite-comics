<script>
import AppSeries from './AppSeries.vue';

export default {
    name: "AppMain",
    components: {
      AppSeries
    },
    data() {
      return {
        series: [
            {
                  thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
                  price: '$19.99',
                  series: 'Action Comics',
                  type: 'comic book',
              },
              {
                  thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
                  price: '$3.99',
                  series: 'American Vampire 1976',
                  type: 'comic book',
              },
              {
                  thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
                  price: '$16.99',
                  series: 'Aquaman',
                  type: 'graphic novel',
              },
              {
                  thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
                  price: '$2.99',
                  series: 'Batgirl',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
                  price: '$3.99',
                  series: 'Batman',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
                  price: '$2.99',
                  series: 'Batman Beyond',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
                  price: '$3.99',
                  series: 'Batman/Superman',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
                  price: '$4.99',
                  series: 'Batman/Superman Annual',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
                  price: '$5.99',
                  series: 'Batman: The Joker War Zone',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
                  price: '$6.99',
                  series: 'Batman: Three Jokers',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
                  price: '$4.99',
                  series: 'Batman: White Knight Presents: Harley Quinn',
                  type: 'comic book',
              },
              {
                  thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
                  price: '$16.99',
                  series: 'Catwoman',
                  type: 'graphic novel',
                },
            ]
      }
    }
}
</script>

<template>
  <main>
    <div class="container-main">
      
     <span class="label lbl-current">CURRENT SERIES</span>
      <div class="row-card">
        <AppSeries v-for="(serie, index) in series" :key="index" :thumb="serie.thumb" :serie="serie.series"/>
      </div>
      <button class="label">LOAD MORE</button>
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;

main {
  width: 100%;
  padding: 50px;
  background-color: #1C1C1C;
  font-size: 1.2rem;
  font-weight: bold;
  position: relative;
}
.row-card {
  @include flex;
  flex-wrap: wrap;
  flex-direction: row;
  align-items: stretch;
}
.container-main {
  @include margin;
  color: white;
}

button {
  position: absolute;
  left: 900px;
}
.label {
  background-color: #0C7CEC;
  color: white;
  padding: 10px 45px;
  font-weight: bold;
}

.lbl-current {
  position: absolute;
  top: -25px;
}

</style>