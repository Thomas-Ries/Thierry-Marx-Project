<template>
  <div class="register">
<img class="background-register" src="../../public/Img/ail.jpeg" alt="">
<registerNavbar />

<section class="register-block">
    <h1>INSCRIPTION</h1>
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

            <div class="form-group">
                <label for="exampleInputPassword1">Confirmation du mot de passe</label>
                <input type="password" class="form-control" id="exampleInputPassword1" placeholder="">
            </div>

            <div class="form-group form-check">
                <p class="redirection" for="exampleCheck1">Déjà inscrit ? <router-link to="/login"> Se connecter </router-link> </p>
            </div>

            <button type="submit" class="btn btn-primary">Inscription</button>
        </form>

</section>
  </div>
</template>

<script>
import registerNavbar from "../components/navbar/registerNavbar";

export default {
  name: "register",
  components: {
      registerNavbar,
  }
}
</script>

<style scoped>

.background-register {
    height: 100vh;
    width: 100%;
    object-fit: cover;
    opacity: .86;
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