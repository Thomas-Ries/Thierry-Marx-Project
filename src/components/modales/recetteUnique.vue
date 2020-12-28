<template>
<div class="bloc-modale" v-if="revele">
    <div class="overlay" @click="toggleModale"></div>
    <div class="modale card">
        <router-link to="/"><img class="logo" src="Img/Logo.png" alt="" height="45px"></router-link>
        <div @click="toggleModale" class="btn-modale btn btn-danger"> X </div>


            <section class="content">
                <img src="../../../public/Img/sauce.jpeg" alt="">
                <div class="ingredients">
                    <h2>INGRÉDIENTS</h2>
                    <p> Tofu </p>
                    <p> Sucre complet - 2càs </p>
                    <p> Lait de coco - 400ml </p>
                    <p> Bouillon de Légumes - 700ml </p>
                    <p> Citronelle </p>
                    <p> Pâte de curry rouge - 2-3càs </p>
                    <p> Citron vert - jus d'un citron </p>
                    <p> Coriandre fraîche </p>
                    <p> Sauce Soja - 1càs </p>
                    <p> Sauce poisson (nuoc mam) - 3càs </p>
                    <p> Curcuma - 1càs </p>
                    <p> Poivre - 1 tour de moulin </p>
                    <p> Ail - 1 petite gousse </p>
                </div>

                <div class="main-content">
                    <div class="title">
                        <h1>Effusion de Sauce Canard Laqué</h1>
                        <h4><i class="far fa-hourglass"></i>Temps de préparation : 1h15</h4>
                        <h4><i class="fas fa-star"></i>Difficulté :  
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        </h4>
                        <h4><i class="fas fa-users"></i>Pour 4 personnes </h4>
                    </div>
                    <div class="etapes">
                        <h2>ÉTAPES</h2>
                        <p>Émincez très finement le tofu, coupez l'aubergine en dés</p>
                        <p>Dans une poêle, faites chanter l'huile puis faites dorer le tofu et l'aubergine</p>
                        <p>Reservez</p>
                        <p>Dans un wok, faites chauffer 2càs de lait de coco et de la pâte de curry (moi j'en mets 4-5 càs mais allez y progressivement pour ne pas avoir "trop chaud" au moment de déguster le plat)</p>
                        <p>Vous pouvez commencer par mettre 2 càs et vous ré-ajusterez si besoin .</p>
                        <p>Versez le reste de lait de coco / mélangez/goutez en en fonction ajoutez ou non de la pâte de curry</p>
                        <p>Portez à ébullition</p>
                        <p>Déposez les dés d'aubergines et laissez mijoter 10-15 minutes</p>
                        <p>Ajoutez la viande et cuire encore 3-4 minutes</p>
                        <p>Assaisonnez avec la sauce poisson (petit à petit, goûtez, ajoutez...)</p>
                        <p>Saupoudrez de feuilles de basilic ciselées et de 1/2 tomates cerises</p>
                        <p>Servir avec du riz Jasmin</p>
                        <p>Dégustez chaud!</p>

                    </div>
                </div>
            </section>

    </div>
    
    
</div> 



</template>

<script>
export default {
    name: "recetteUnique",
    props: {
        revele: Boolean,
        toggleModale: Function,
    }

}
</script>

<style scoped>
.bloc-modale {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.overlay {
    background: rgba(0,0,0,0.5);
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.modale {
    background: #3c2a4d;
    color: #333;
    padding: 5rem;
    position: fixed;
    top: 13%;
    width: 150rem;
    height: 80rem;
}

.logo {
    position: absolute;
    top: 10px;
    left: 10px;
}

.btn-modale {
    position: absolute;
    top: 10px;
    right: 10px;
    font-size: 2rem;
}

.content {
    display: flex;
    justify-content: space-between;
}

.content img {
    margin-top: 2rem;
    height: 70rem;
    width: 50rem;
    object-fit: cover;
    border-radius: 5px;
}

.ingredients {
    position: absolute;
    top: 29rem;
    left: 60rem;
    color: #fff;
    width: 25rem;
}

.ingredients h2 {
    font-size: 2rem;
    text-decoration: underline;
    color: var(--title);
}

.ingredients p,
.etapes p {
    font-size: 1.6rem;
    line-height: 1.5rem;
}

.ingredients p:nth-child(2),
.etapes p:nth-child(2) {
    margin-top: 2rem;
}

.main-content {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 10rem;
    left: 88rem;
    color: #fff;
    width: 58rem;
}

.main-content h1 {
    color: var(--title);
    font-size: 4rem;
    text-decoration: underline;
}

.fa-hourglass {
    font-size: 1.5rem;
    margin-right: 2rem;
}

.fa-star {
    font-size: 1.5rem;
    margin-right: 1.2rem;
}
.fa-star:nth-child(2) {
    margin-left: 1.3rem;
}

.fa-users {
    font-size: 1.5rem;
    margin-right: 1.1rem;
}

.main-content h4 {
    text-align: left;
    font-size: 2rem;
}

.etapes {
    margin-top: 3.5rem;
}

.etapes h2 {
    font-size: 2rem;
    text-decoration: underline;
    color: var(--title);
}



</style>