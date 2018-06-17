<template>
  <div id="app">
      <Wrapper></Wrapper>    
  </div>
</template>

<script>

  import Wrapper from "./components/Wrapper.vue";

  export default {
    name: 'App',
    components: {
      Wrapper
    }
  }

</script>

<style>

  @import "./assets/css/bootstrap.min.css";
  @import "../node_modules/font-awesome/css/font-awesome.min.css";
  @import "./assets/css/main.css";

</style>

