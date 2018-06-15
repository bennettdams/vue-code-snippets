<template>
  <div id="navbar-mobile">

    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <a class="navbar-brand" href="#">MY WEBSITE</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarToggler" aria-controls="navbarToggler" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarToggler">

        <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
          <NavigationItems></NavigationItems>
        </ul>

      </div>
    </nav>


  </div>
  </template>

  <script>
  import NavigationItems from './NavigationItems.vue'
  export default {
    name: 'NavbarMobile',
    components: {
      NavigationItems
    }
  }
  </script>

  <style scoped>
  </style>
