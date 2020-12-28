<template>
  <div class="recetteNavbar">

<header class="nav-recettes">
        <router-link to="/"><img class="logo" src="Img/Logo.png" alt=""></router-link>
        <nav class="navbar navbar-expand-lg ">
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <router-link to="/le-chef"><a class="nav-link pt-5" href="#">Le Chef</a></router-link>
            </li>
            <li class="nav-item dropdown">
              <router-link to="/recettes"><a class="nav-link pt-5" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Recettes
                <i class="fas fa-angle-down"></i>
              </a></router-link>
              <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#">Entrées</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Salées</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Sucrées</a>
              </div>
            </li>
            <li class="nav-item">
              <a class="nav-link pt-5" href="#">Espace Personnel</a>
            </li>
          </ul>
        </div>
      </nav>
</header>

  </div>

  
</template>

<script>
export default {
    name: "recettesNavbar",

}

</script>

<style scoped>
header {
    background-color: #c7417b;
    height: 5rem;
}

.nav-recettes {
    display: flex;
    justify-content: space-between;
}

.logo {
    margin: .5rem 0 0 1rem;
    height: 4rem;
}

.fas{
    font-size: 1.4rem;
}

.dropdown-item {
    font-size: 1.5rem !important;
    color: #000 !important;
}

.dropdown-item:hover {
  font-weight: 700;
}

.nav-item a {
    color: var(--title) ;
    font-size: 2.5rem;
}
  
.nav-item a:first-child {
    margin-right: 1.5rem;
}

</style>