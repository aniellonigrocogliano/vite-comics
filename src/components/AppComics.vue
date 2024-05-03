<script>
export default {
    props: {
      itemThumb: String,
      itemPrice: String,
      itemSeries: String,
      itemType: String,
    },
  };
  </script>
  
  <template>

      <div >
        <h3>{{ itemSeries }}</h3>
        <p>{{ itemPrice }}</p>
      </div>
  
  </template>
  
  <style scoped lang="scss">

  </style>