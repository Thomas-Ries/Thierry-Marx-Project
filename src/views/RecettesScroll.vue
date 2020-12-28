<template>
  <div class="recettesScroll">
      <recettesNavbar />
    
    <section>
        <div class="main-container">
            <h1 class="ml-5"> Mes Recettes</h1>
        </div>
    
        <div class="recettes main-container">
        <squareRecette />
        </div>

        <nav aria-label="...">
            <ul class="pagination pagination-lg">
                <li class="page-item"><a class="page-link" href="#">1</a></li>
                <li class="page-item"><a class="page-link" href="#">2</a></li>
                <li class="page-item"><a class="page-link" href="#">3</a></li>
                <li class="page-item"><a class="page-link" href="#">4</a></li>
                <li class="page-item"><a class="page-link" href="#">Suivant<i class="fas fa-angle-right"></i></a></li>
            </ul>
        </nav>


    </section>
  </div>
</template>

<script>
import recettesNavbar from "../components/navbar/recettesNavbar";
import squareRecette from "../components/recettes/squareRecette";


export default {
    name: "RecettesScroll",
    components : {
        recettesNavbar,
        squareRecette,
    },

}
</script>


<style scoped>
section {
    background-color: #3c2a4d;
    height: auto;
    padding-bottom: 10rem;
}

.main-container {
    width: 140rem;
    margin: auto;
}

h1 {
    text-decoration: underline;
    font-size: 3rem;
    color: #fff !important;
    padding-top: 8rem;
    font-weight: 300;
    margin-left: -.3rem !important;
}

nav {
    margin-left: 75rem;
    margin-top: 5rem;
    border-radius: none !important;
}

.page-item {
    margin-left: 2rem;
}

.page-item a {
    font-size: 2.5rem !important;
    background-color: #696D7D;
    color: var(--paragraph);
    border: none;
}

.page-item a:hover {
    border: 1px solid #fff;
    background-color: #fff;
    color: #000;
    font-weight: 800;
}

.fa-angle-right {
    font-size: 2rem;
    margin-left: 1rem;
}

</style>