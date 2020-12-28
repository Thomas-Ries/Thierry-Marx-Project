<template>
  <div class="home">
  <mainNavbar />
    <img class="background" src="Img/plat3.jpeg" alt="">
  <section class="home-title">
    <h1 class="big-title">La cuisine Molléculaire enseignée par</h1>
    <h2 class="small-title">Thierry Marx</h2>
    <router-link to="/le-chef"><button type="button" class="btn btn-warning">Bienvenue</button></router-link>
  </section>
  </div>
</template>

<script>
import mainNavbar from "../components/navbar/mainNavbar";
import { gsap } from 'gsap';

export default {
  name: 'Home',

  components: {
    mainNavbar,
  },

  mounted() {
    this.startAnimations()
  },

  methods: {
    startAnimations() {
    gsap.from('.big-title', {
      duration: 2,
      opacity: 0,
      y: -200,
      // ease: 'Power2.In'
    }),

    gsap.from('.small-title', {
      duration: 2,
      opacity: 0,
      y: -170,
      // ease: 'Power2.In'
    }),

    // gsap.from('.btn', {
    //   duration: 1,
    //   opacity: 0,
    //   y: 50,
    //   delay: 2.2
    // }),
    gsap.from('.btn', {
      opacity: 0,
      duration: 10,
      delay: 2,
    })

    }
    },
  }

</script>

<style scoped>
.background {
    height: 100vh;
    width: 100%;
    object-fit: cover;
  }
  
  .home-title {
    position: absolute;
    top: 30rem;
    right: 30rem;
    display: flex;
    flex-direction: column;
  }
  
  .home-title h1 {
    font-size: 4rem;
    color: var(--paragraph);
    width: 40rem;
  }
  
  .home-title h2 {
    font-family: 'Tangerine', sans-serif;
    font-size: 7rem;
    color: var(--signature);
    margin: 3rem 0 0 5rem;
  }

  .btn-warning {
    font-size: 2rem;
    height: 11rem;
    width: 11rem;
    margin: 7rem 0 0 13rem;
    background-color: transparent;
    color: #fff;
    border: 1px solid #fff;
    border-radius: 50%
  }

  .btn-warning:hover {
    color: var(--btn);
    font-weight: 500;
    background-color: transparent;
    transition: color .5s;
    border: 1px solid #fff;

    /* box-shadow: .5px .5px 10px var(--btn); */
  }
  
</style>
