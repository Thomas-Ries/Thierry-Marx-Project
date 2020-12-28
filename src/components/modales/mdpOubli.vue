<template>
<div class="bloc-modale" v-if="revele">
    <div class="overlay" @click="toggleModale"></div>
    <div class="modale card">
        <div @click="toggleModale" class="btn-modale btn btn-danger"> X </div>

            <div class="form-group">
                <h2>Mot de passe oublié </h2>
                <label class="mt-3 mb-1" for="exampleInputEmail1">Adresse mail</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="ex: john@mail.com">
                <button type="submit" class="btn btn-primary">Connexion</button>

            </div>

    </div>
    
    
</div> 



</template>

<script>
export default {
    name: "mdpOublie",
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
    background: #f1f1f1;
    color: #333;
    padding: 5rem;
    position: fixed;
    top: 30%;
    width: 35rem;
}

.btn-modale {
    position: absolute;
    top: 10px;
    right: 10px;
}

.form-group {
    text-align: center;
}

.form-group h2 {
    font-size: 2.5rem;
}

.form-group label {
    color: #000;
    font-size: 1.8rem;
}

.form-group input {
    margin-bottom: 2rem;
    height: 3.5rem;
    background-color: lightgrey;
    font-size: 1.4rem;
    color: #000;
}
.btn-primary {
    font-size: 2rem;
    width: 12rem;
    height: 4rem;
    background-color: var(--btn);
    border: none;
}

.btn-primary:hover {
    color: #000;
    font-weight: 700;
    background-color: var(--btn);
}

</style>