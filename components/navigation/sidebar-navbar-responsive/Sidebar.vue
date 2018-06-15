<template>
  <!-- <div id="sidebar"> -->

      <div class="py-2 sticky-top">

        <a class="navbar-brand mx-0 px-0" href="#">
          <img class="img-fluid" src="">
        </a>

        <div class="nav flex-column">
          <NavigationItems></NavigationItems>
        </div>

      </div>


  <!-- </div> -->
  </template>

  <script>
  import NavigationItems from './NavigationItems.vue'
  export default {
    name: 'Sidebar',
    components: {
      NavigationItems
    }
  }
  </script>

  <style scoped>
  </style>
