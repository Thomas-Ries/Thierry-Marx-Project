<template>
  <div class="topbar">
    <router-link to="/"><img class="logo" src="Img/Logo.png" alt=""></router-link>

    <nav class="navbar navbar-expand-lg">
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <router-link to="/login"><a class="nav-link"> Connexion </a></router-link>
          </li>

        </ul>
      </div>
    </nav>

  </div>
</template>

<script>
export default {
  name: 'registerNavbar',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background {
    height: 100vh;
    width: 100%;
    object-fit: cover;
  }
  
  .logo {
    position: absolute;
    top: 1.5rem;
    left: 1.5rem;
  }
  
  .navbar {
    position: absolute;
    top: 0;
    right: 2rem;
  }
  
  .nav-item a {
    color: var(--title) ;
    font-size: 2.5rem;
  }
  
  .nav-item a:first-child {
    margin-right: 1.5rem;
  }
</style>
