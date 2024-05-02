<script>
export default {
    data() {
    return {
    dcComics: [
      "Characters",
      "Comics",
      "Movies",
      "TV",
      "Games",
      "Videos",
      "News"
    ],
    shop: [
      "Shop DC",
      "Shop DC Collectibles"
    ],
    Dc: [
      "Terms Of Use",
      "Privacy policy (New)",
      "Ad Choices",
      "Advertising",
      "Jobs",
      "Subscriptions",
      "Talent Workshops",
      "CPSC Certificates",
      "Ratings",
      "Shop Help",
      "Contact Us"
    ],
    Sites: [
      "DC",
      "MAD Magazine",
      "DC Kids",
      "DC Universe",
      "DC Power Visa"
    ],
    socialImg: [
      'facebook',
      'periscope',
      'pinterest',
      'twitter',
      'youtube'
    ]
};
  },
  methods: {
    getImagePath(imageName) {
      return new URL(`../assets/img/footer-${imageName}.png`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <footer> 
    <section>
    <div> 
    <ul ><h2>DC COMICS</h2> 
      <li v-for="item in dcComics">
        <a href="" >{{item}}</a>
      </li>
    </ul>
    <ul ><h2>SHOP</h2> 
      <li v-for="item in shop">
        <a href="" >{{item}}</a>
      </li>
    </ul>
</div>
<div> 
    <ul ><h2>DC</h2> 
      <li v-for="item in Dc">
        <a href="" >{{item}}</a>
      </li>
    </ul>
</div>
<div> 
    <ul ><h2>SITES</h2> 
      <li v-for="item in Sites">
        <a href="" >{{item}}</a>
      </li>
    </ul>
</div>
</section>
<section>
    <img
        src="../assets/img/dc-logo-bg.png"
        alt="Logo DC Comics"
      />
</section>
<section class="social">
    <div><a href="#" class="button">SIGN-UP NOW!</a></div>
    <div>
        <div> 
    <ul ><h2>FOLLOW US</h2> 
      <li v-for="item in socialImg">
        <a href="" ><img :src="getImagePath(item)" alt="{{item}}" /></a>
      </li>
    </ul>
</div>
    </div>
</section>
<section class="footer-end"></section>
  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
footer{ 
    @include flex(row, space-around, flex-start);
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
   section{width:35%;
    padding:15px;
        @include flex(row, space-around, flex-start);
    }
    h2{
        color:$white; 
    }
    ul {
    
    list-style-type: none;
    gap: 0.1rem;
    
    a {
      padding: 2px 2px;
      text-decoration: none;
      display: inline-block;
      color: $grayFooter;
      font-size: 0.8rem;
    }
}
.social{
    @include flex(row, space-around, flex-start);
    position:absolute;
    height:150px;
    width:100%;
    background-color:$graySocial;
    bottom:0px;
    .button{
        border:2px solid $blu;
  color: $white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
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
.footer-end{
    position:absolute;
    background-color: $black;
    width:100%;
    height:15px;
    bottom:0px;
}
}
</style>