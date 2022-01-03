<template>
  <div id="app">
    <header>
      <router-link @click="close" to="/"><img id="logo-header" src="@/assets/img/logos/blanc-seul.svg" alt="">
      </router-link>
      <nav>
        <div id="burger-menu">
          <div class="nav-toggle" onclick="document.documentElement.classList.toggle('menu-open')">
            <div class="nav-toggle-bar"></div>
          </div>
          <div class="menu">
            <ul>
              <li @click="close()">
                <router-link to="/">
                  <img id="logo-burger" src="@/assets/img/logos/noir-seul.png" alt="">
                </router-link>
              </li>
              <li @click="close()">
                <router-link class="lien" to="/news">
                  <img id="news" class="img-fluid" src="@/assets/img/icons/Icon_black_newspaper.svg" alt="">
                  Actualités
                </router-link>
              </li>
              <li @click="close()">
                <router-link class="lien" to="/about">
                  <img class="img-fluid" src="@/assets/img/icons/Icon_black_info.svg" alt="">
                  À propos
                </router-link>
              </li>
              <li @click="close()">
                <img src="@/assets/img/icons/Icon_black_contacts.svg" alt="">
                <p class="lien">Contact</p>
              </li>
              <li>
                <router-link class="lien" to="/Profile">
                  <img data-toggle="modal" data-target="#cnxModal" src="@/assets/img/composants/se_connecter_black.svg" @click="close()"
                       alt="Se connecter">
                </router-link>

              </li>
            </ul>
          </div>
        </div>
        <div class="nav-bar">
          <div>
            <ul>
              <li>
                <img src="@/assets/img/icons/Icon_newspaper.svg" alt="">
                <router-link class="lien" to="/news">Actualités</router-link>
              </li>
              <li>
                <img src="@/assets/img/icons/Icon_info.svg" alt="">
                <router-link class="lien" to="/about">À propos</router-link>
              </li>
              <li>
                <img class="img-fluid" src="@/assets/img/icons/Icon_contacts.svg" alt="">
                <a class="lien">Contact</a>
              </li>
              <li>
                <img data-toggle="modal" data-target="#cnxModal" id="connexion-icon" src="@/assets/img/composants/se_connecter.svg" alt="Se connecter">
              </li>
            </ul>
          </div>
        </div>

      </nav>
    </header>
    <router-view/>
    <!-- Modal connexion -->
    <div
        class="modal fade"
        id="cnxModal"
        ref="cnxModal"
        tabindex="-1"
        role="dialog"
        aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Connexion à l'application</h5>

            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>

          <div class="modal-body">

            <div class="input-group mb-3">
              <div class="input-group-prepend">
                <span class="input-group-text">Login</span>
              </div>
              <input type="text" class="form-control" placeholder="Login"
                     v-model="utilisateur.username"
              >
            </div>

            <div class="input-group mb-3">
              <div class="input-group-prepend">
                <span class="input-group-text">Mot de passe</span>
              </div>
              <input type="text" class="form-control" placeholder="Mot de passe"
                     v-model="utilisateur.password"
              >
            </div>

          </div>

          <!--            <div v-if="message != null" class="alert alert-warning text-center" role="alert">-->
          <!--              {{message}}-->
          <!--            </div>-->

          <div class="modal-footer">
            <button type="button" class="btn btn-dark"
                    @click="deconnect" data-dismiss="modal">
              Deconnexion</button>

            <button type="button" class="btn btn-dark"
                    @click="connect"
            >
              Connexion</button>
          </div>
        </div>
      </div>
    </div>
    <!-- Modale erreur -->
    <div
        class="modal fade"
        id="errorModal"
        ref="errorModal"
        tabindex="-1"
        role="dialog"
        aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content" style="background-color:transparent!important;">
          <div class="modal-body">
            <!--              <div v-if="message != null"-->
            <!--                   class="alert alert-warning text-center" role="alert">-->
            <!--                {{message}}-->
            <!--              </div>-->
          </div>
        </div>
      </div>
    </div>
    <footer>
      <img id="logo-footer" src="@/assets/img/logos/Global-blanc.svg" alt="">
      <div id="left-block">
        <ul>
          <li>
            <router-link class="lien" to="/news">Actualités</router-link>
          </li>
          <li>
            <router-link class="lien" to="/about">À propos</router-link>
          </li>
        </ul>
      </div>
      <div id="right-block">
        <ul>
          <li>
            <router-link class="lien" to="/mentions">Mentions légales</router-link>
          </li>
          <li>
            <p class="lien">Nous Contacter</p>
          </li>
        </ul>
      </div>
    </footer>
  </div>
</template>

<style lang="less">
</style>
<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      utilisateur:{
        username:null,
        password:null,
      },
      visible: false,
    }
  },
  created() {

  },
  methods: {
    connect:function(){},
    deconnect:function(){},
    close() {
      console.log("ca ferme");
      document.documentElement.classList.remove('menu-open')
    }
  }
}
</script>
<style>
@import "assets/css/styles.css";
@import "assets/css/menu.css";
</style>