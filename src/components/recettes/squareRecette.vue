<template>
  <div class="recette">
        <div class="square">
          <h3> Effusion de Sauce Canard Laqué</h3>
          <img @click="toggleModale" src="../../../public/Img/sauce.jpeg" alt="">
          <recetteUnique v-bind:revele="revele" v-bind:toggleModale="toggleModale" />
        </div>

        <div class="square">
          <h3> Tian & ses Perles de Champagne</h3>
          <img src="../../../public/Img/plat1.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Fleurs Gelées sur lit de Légumes rôtis Glacés</h3>
          <img src="../../../public/Img/plat4.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Passé de Butternut Coco  & bâtonnets de Carottes</h3>
          <img src="../../../public/Img/plat5.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Rouleaux de Printemps façon Baiser du Dragon</h3>
          <img src="../../../public/Img/plat6.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Demi de Fânes de Carottes en Émulsion </h3>
          <img src="../../../public/Img/plat8.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Roulé de Porc dans en Chou et Sauce Chasseur</h3>
          <img src="../../../public/Img/presentation2.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Sushis à l'Azote</h3>
          <img src="../../../public/Img/plat7.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Cocktail Sucré / Salé & Perles de Tapioca</h3>
          <img src="../../../public/Img/drink.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Asperges vertes en demi-cuisson Azotée</h3>
          <img src="../../../public/Img/asperges-vertes.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Composition Florale à déguster</h3>
          <img src="../../../public/Img/composition.jpeg" alt="">
        </div>

        <div class="square">
          <h3> Été Croquant Recomposé</h3>
          <img src="../../../public/Img/plat9.jpg" alt="">
        </div>
  </div>
</template>

<script>
import recetteUnique from "../modales/recetteUnique";
// import { gsap } from 'gsap';


export default {
    name: "squareRecette",
    components: {
        recetteUnique,
    },

    data() {
        return {
            revele: false,
        }
    },



    methods: {
        toggleModale: function() {
            this.revele = !this.revele;
        },
    }

}
</script>

<style scoped>

.recette {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.square img
{
    height: 30rem;
    width: 40rem;
    margin-bottom: 5rem;
    object-fit: cover;
    transition-delay: .5s;
    transition-duration: 1s;
    border-radius: 5px;
}

.square img:hover {
  cursor: pointer;
  border-radius: 5px;
  transform: scale(1.07);
}

.square h3 {
    margin-top: 5rem;
    margin-left: .5rem;
    color: #fff;
    font-size: 2rem;
    font-weight: 200;
}

</style>