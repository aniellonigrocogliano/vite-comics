<script>
export default {
    props: {
      itemThumb: String,
      itemPrice: String,
      itemSeries: String,
      itemType: String,
    },
 
  
  methods: {
    getImagePath(imageName) {
      return new URL(`${imageName}`, import.meta.url).href;
    },
    
  },
};
  </script>
  
  <template>

      <div class="row" >
        <div class="card">
        <img :src="getImagePath(itemThumb)" :alt="itemSeries" />
        <h5> {{ itemSeries }}</h5>
        <p>Genere: {{ itemType }}</p>
        <p>Prezzo: {{ itemPrice }}</p>
        
    </div></div>
  
  </template>
  
  <style scoped lang="scss">
  @use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.row{
    color:$white;
    width:16%;
    img{
        width:100%;
    }
    .card{
        padding:20px;
        h5{
            font-size: 0.9rem;
        }
        p{
            font-size: 0.7rem;
        }
    }
}

  </style>