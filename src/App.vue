<template>
  <div id="app">
    <header>
      <router-link to="/"><img id="logo-header" src="@/assets/img/logos/blanc-seul.svg" alt=""></router-link>
      <nav>
        <div>
          <div class="nav-toggle" onclick="document.documentElement.classList.toggle('menu-open')">
            <div class="nav-toggle-bar"></div>
          </div>
          <div class="menu">
            <ul>
              <li @click="close()" >
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
              <li>
                <img class="img-fluid" src="@/assets/img/icons/Icon_black_contacts.svg" alt="">
                <p class="lien" @click="visible=true;close()">Contact</p>
              </li>
              <li>
                <img src="@/assets/img/composants/se_connecter_black.svg" alt="Se connecter">
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
                <img src="@/assets/img/icons/Icon_contacts.svg" alt="">
                <p class="lien" @click="visible=true;close()">Contact</p>
              </li>
              <li>
                <img src="@/assets/img/composants/se_connecter.svg" @click="close()" alt="Se connecter">
              </li>
            </ul>
          </div>
        </div>
      </nav>
      <div v-show="visible" id="contact">
        <span @click="visible=false">close</span>
      </div>
    </header>
    <router-view/>
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
            <p class="lien" @click="visible=true">Nous Contacter</p>
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
  components: {},
  data() {
    return {
      visible: false,
    }
  },
  methods:{
    close(){
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