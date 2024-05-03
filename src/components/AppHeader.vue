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
  height: 130px;
line-height: 80px;
    .section-header{width:70%;
        @include flex(row, space-between, center);
        padding: 15px;
}
    
  .logo {
    text-align: center;
    padding-top: 50px;
    &:hover {
      opacity: 0.5;
    }
  }
  ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 0.5rem;
    margin-top: 26px;

    a {
      padding: 10px 16px;
      text-decoration: none;
      display: inline-block;
      color: $gray;
      font-weight:900;

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