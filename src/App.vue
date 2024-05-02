<script>
import AppHeader from './components/AppHeader.vue';
import AppStar from './components/AppStar.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

  export default {
  components: {
    AppHeader,
    AppStar,
    AppMain,
    AppFooter,
  }

}
</script>

<template>
<AppStar />
<AppHeader />
<AppMain />
<AppFooter />



</template>

<style lang="scss">


</style>