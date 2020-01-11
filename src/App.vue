<template>

  <div id="app">

    <navbar></navbar>
    <router-link />

  </div>

</template>

<script>

import Navbar from "@/components/navbar";

export default {
  name: "App",
  components: {
    // Vue.js application infers automatically that the <navbar> HTML tag corresponds to the Navbar component
    navbar: Navbar
  }
};

</script>

<style>

</style>
