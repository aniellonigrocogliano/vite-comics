<script>
export default {
  data() {
    return {
      menu: [
        {
          title: "CHARACTERS",
          isActive: false,
        },
        {
          title: "COMICS",
          isActive: true,
        },
        {
          title: "MOVIES",
          isActive: false,
        }, 
        {
          title: "TV",
          isActive: false,
        },
        {
          title: "GAMES",
          isActive: false,
        },
        {
          title: "COLLECTIBLES",
          isActive: false,
        },
        {
          title: "VIDEOS",
          isActive: false,
        },
        {
          title: "FANS",
          isActive: false,
        },
        {
          title: "NEWS",
          isActive: false,
        },
        {
          title: "SHOP",
          isActive: false,
        },
     
      ],
    };
  },
};
</script>

<template>
  <header>
    <section class="section-header">
    <div class="logo">
      <img
        src="../assets/img/dc-logo.png"
        alt="Logo DC Comics"
      />
    </div>
    <ul class="navigation">
      <li v-for="item in menu">
        <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
      </li>
    </ul>
</section>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
header { @include flex(row, center, center);
    
    .section-header{width:80%;
        @include flex(row, space-between, center);
        padding: 15px;
}
    
  .logo {
    text-align: center;
  }
  ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 0.5rem;
    margin-top: 26px;
    font-weight: bold;

    a {
      padding: 10px 16px;
      text-decoration: none;
      display: inline-block;
      color: $gray;

      &:hover {
        color:$blu;
      }

      &.active {
        color:$blu;
        border-bottom: 5px solid $blu;
      }
    }
  }

}

</style>