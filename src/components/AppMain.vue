<script>
import AppComics from './AppComics.vue';
export default {
  components: {
    AppComics,
  },
    data() {
    return {
        ArrayComics: [
  {
      thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
      price: "$19.99",
      series: "Action Comics",
      type: "comic book",
  },
  {
      thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
      price: "$3.99",
      series: "American Vampire 1976",
      type: "comic book",
  },
  {
      thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
      price: "$16.99",
      series: "Aquaman",
      type: "graphic novel",
  },
  {
      thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
      price: "$2.99",
      series: "Batgirl",
      type: "comic book",
  },
  {
      thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
      price: "$3.99",
      series: "Batman",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
      price: "$2.99",
      series: "Batman Beyond",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
      price: "$3.99",
      series: "Batman/Superman",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
      price: "$4.99",
      series: "Batman/Superman Annual",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
      price: "$5.99",
      series: "Batman: The Joker War Zone",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
      price: "$6.99",
      series: "Batman: Three Jokers",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
      price: "$4.99",
      series: "Batman: White Knight Presents: Harley Quinn",
      type: "comic book",
  },
  {
      thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
      price: "$16.99",
      series: "Catwoman",
      type: "graphic novel",
  },
],
};
    },
};
</script>

<template>
    <div class="jumbotron">
        <div><a href="#" class="button">CURRENT SERIES</a></div>
    </div>
    <main>
        <div class="container">
  <AppComics 
  v-for="item in ArrayComics"
        :itemThumb="item.thumb"
        :itemPrice="item.price"
        :itemSeries="item.series"
        :itemType="item.type"
  />
  <div><a href="#" class="button">LOAD MORE</a></div>
        </div>
        
    </main>
    
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.jumbotron{ position: relative;
    height:25vh;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    .button{
        position:absolute;
        bottom:-30px;
        left:15%;
        font-weight:900;
        border:2px solid $blu;
  color: $white;
  background-color: $blu;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  margin: 4px 2px;
  cursor: pointer;
    }
}
main{ @include flex(row, space-around, center);
    background-color: $black;
    h2{
        color:$white;
    }
    .container{
        @include flex(row, space-around, center);
        width:70%;
        flex-wrap: wrap;
    }
    .button{
        border:2px solid $blu;
  color: $white;
  background-color: $blu;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  margin: 4px 2px;
  cursor: pointer;
  padding:5px;
  margin-bottom:30px;
  font-weight:900;
    }
    a:hover {
      opacity: 0.5;
      }
    h2{
        color:$blu;
    }
    ul{
        @include flex(row, space-around, center);
        list-style-type: none;
    gap: 0.5rem;
    margin-top: 26px;
    }
}
</style>