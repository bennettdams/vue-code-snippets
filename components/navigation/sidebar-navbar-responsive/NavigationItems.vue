<template>
  <div id="navigation-items">

          <li class="nav-item">
            <router-link to="/" class="nav-link text-white">
              <i class="fas fa-home fa-fw text-primary"></i><span class="pl-3">HOME</span>
            </router-link>
          </li>

          <li class="nav-item">
            <router-link to="/about" class="nav-link text-white">
              <i class="fas fa-code-branch fa-fw text-success"></i><span class="pl-3">ABOUT</span>
            </router-link>
          </li>

  </div>
  </template>

  <script>
  export default {
    name: 'NavigationItems',
    methods: {
    }
  }
  </script>

  <style scoped>
    .nav-item:hover {
      background-color: rgba(255, 255, 255, 0.2);
    }

    .nav-link {
      font-size: 0.9rem;
    }
  </style>
