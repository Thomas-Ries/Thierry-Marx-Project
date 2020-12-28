<template>
<div class="login">

<img class="background-login" src="../../public/Img/epices.jpeg" alt="">

<loginNavbar />

<section class="register-block">
    <h1>CONNEXION</h1>
        <form>
            <div class="form-group">
                <label for="exampleInputEmail1">Adresse mail</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="ex: john@mail.com">
                <!-- <small id="emailHelp" class="form-text text-muted">Nous ne partageons pas vos données.</small> -->
            </div>

            <div class="form-group">
                <label for="exampleInputPassword1">Mot de passe</label>
                <input type="password" class="form-control" id="exampleInputPassword1" placeholder="">
            </div>

            <a @click="toggleModale" href="#" class="mdp-oublie form-text">Mot de passe oublié ?</a>

            <div class="form-group form-check">
                <p class="redirection mt-5" for="exampleCheck1">Pas encore de compte ? <router-link to="/register">S'inscrire</router-link>  </p>
            </div>

            <button type="submit" class="btn btn-primary">Connexion</button>
        </form>

</section>

<mdp-oubli v-bind:revele="revele" v-bind:toggleModale="toggleModale" />

</div>
</template>

<script>
import loginNavbar from "../components/navbar/loginNavbar";
import mdpOubli from "../components/modales/mdpOubli";


export default {
    name: "login",

    components: {
        loginNavbar,
        mdpOubli,
    },

    data() {
        return {
            revele: false,
        }
    },

    methods: {
        toggleModale: function() {
            this.revele = !this.revele;
        }
    }

}
</script>

<style scoped>
.background-login {
    height: 100vh;
    width: 100%;
    object-fit: cover;
    opacity: .86;
}

.mdp-oublie {
    padding-left: 7rem;
    color: var(--paragraph);
    font-size: 1.5rem;
    margin: -2rem 0 0 0;
}

.mdp-oublie:hover {
    color: var(--paragraph);
}

.register-block {
    position: absolute;
    top: 30rem;
    left: 0;
    right: 0;
    margin: auto;
    display: flex;
    flex-direction: column;
    width: 27rem;
}

.register-block h1 {
    font-size: 4rem;
    text-align: center;
    color: var(--paragraph);
    margin-bottom: 2rem;
}

.form-group {
    text-align: center;
}

.form-group label {
    color: var(--paragraph);
    font-size: 2rem;
}

.form-group input {
    margin-bottom: 2rem;
    height: 3.5rem;
    background-color: lightgrey;
    font-size: 1.4rem;
    color: #000;
}

.redirection {
    font-size: 1.4rem;
    color: var(--paragraph);
    margin-top: -2rem;
    margin-bottom: 4rem;
}

.form-group a {
    color: var(--title);
    font-size: 1.4rem;
}

.btn-primary {
    font-size: 2rem;
    width: 20rem;
    height: 4rem;
    margin-left: 3.5rem;
    background-color: var(--btn);
    border: none;
}

.btn-primary:hover {
    color: #000;
    font-weight: 700;
    background-color: var(--btn);
}

</style>