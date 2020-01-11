<!-- HTML we wish to render for our component within the <template> -->
<template>
  <div class="pure-menu pure-menu-horizontal">
    <div class="container">
      <a href="#" class="pure-menu-heading pure-menu-link">Home</a>
      <ul class="pure-menu-list">
        <li class="pure-menu-item">
          <a href="#" class="pure-menu-link">News</a>
        </li>
        <li class="pure-menu-item">
          <a href="#" class="pure-menu-link">Sports</a>
        </li>
        <li class="pure-menu-item">
          <a href="#" class="pure-menu-link">Finance</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<!-- define all of our core component functionality, a.k.a. all of the JavaScript functions within the <script> tags -->
<script>
  export default {
    name: "Navbar",
  };

</script>
<style scoped>
  .pure-menu {
    background-color: #e17842;
  }
  .pure-menu a {
    color: white;
  }
</style>
