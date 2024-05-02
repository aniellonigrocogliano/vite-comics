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
};
  },
};
</script>

<template>
  <footer> 
    <div> 
    <ul ><h2>DC COMICS</h2> 
      <li v-for="item in dcComics">
        <a href="" >{{item}}</a>
      </li>
    </ul>
</div>
<div> 
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
  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
footer{
    background-image: url("../assets/img/footer-bg.jpg");
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
    }
}
}
</style>