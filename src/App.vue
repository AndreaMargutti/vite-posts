<script>
import AppMain from './components/AppMain.vue';

export default {
  data() {
    return {
      
    }
  },
  components: {
    AppMain,
  }
}
</script>

<template>

<h1 class="text-center">
  Sono la pagina principale
</h1>

<AppMain/>

</template>

<style lang="scss">
@use "/node_modules/bootstrap/scss/bootstrap.scss" as *;
@use "src/general.scss" as *
</style>
