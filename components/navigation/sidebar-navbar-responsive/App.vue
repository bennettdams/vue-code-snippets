<template>
<div id="app">

  <div class="container-fluid">
    <div class="row">

      <!-- hide on smaller than tablet -->
      <div class="col-md-2 d-none d-md-block px-1 bg-dark" id="sticky-sidebar">
        <Sidebar></Sidebar>
      </div>

      <!-- show only on mobile -->
      <div class="col-12 d-md-none px-0">
        <NavbarMobile></NavbarMobile>
      </div>

      <div class="col-12 col-md-10" id="main">
        <transition name="fade" mode="out-in" appear>
          <router-view id="view"></router-view>
        </transition>
      </div>
    </div>
  </div>

</div>
</template>

<script>
import Sidebar from './Sidebar.vue'
import NavbarMobile from './NavbarMobile.vue'

export default {
  name: 'app',
  components: {
    Sidebar,
    NavbarMobile
  }
}
</script>

<style>
@import url('https://use.fontawesome.com/releases/v5.0.13/css/all.css');
#main {
  background-color: rgba(240, 242, 245, 1);
}

#sticky-sidebar {
  min-height: 100vh;
}

.fade-enter-active, .fade-leave-active {
  transition-property: opacity;
  transition-duration: .15s;
}

.fade-enter-active {
  transition-delay: .15s;
}

.fade-enter, .fade-leave-active {
  opacity: 0
}

</style>
