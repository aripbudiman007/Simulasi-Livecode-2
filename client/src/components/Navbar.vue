<template>
<!--Navbar-->
    <nav class="navbar navbar-expand-lg navbar-light bg-info">
        <a class="navbar-brand text-white" href="#">Hacktiv Inventory</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
      
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
                <router-link to="/login" class="nav-link text-white" tabindex="-1" aria-disabled="true">Login</router-link>
              </li>
            <li class="nav-item">
              <a class="nav-link text-white" @click="logout" href="#" tabindex="-1" aria-disabled="true">Logout</a>
            </li>
          </ul>
        </div>
      </nav>
</template>

<script>
export default {
  name: 'Navbar',
  methods: {
      logout(){
          this.$store.dispatch('logout')
      }
  }
}
</script>