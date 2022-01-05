<template>
  <div id="home">
    <div id="home-heading">
      <img src="@/assets/img/composants/backgroundvert-accueil.svg" class="background-home">
      <img src="@/assets/img/logos/Global-gris.svg" id="logo-home" class="img-fluid" alt="">
      <img src="@/assets/img/icons/enfants.png" id="kids" alt="">
    </div>
    <p class="text-transition short-title">Découvrez toutes les nouvelles d'E.peri&school le programme éducatif formant
      les enfants au numérique !</p>
    <h1>Evénements à venir</h1>
    <div v-for="media in liste_medias" :key="media.id" class="event-card">
      <img class="event-image" :src=media.acf.file.url alt="">
      <div class="event-title short-title">
        {{media.acf.label}}
      </div>
    </div>
<!--    <div class="event-card">-->
<!--      <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0352.jpg" alt="">-->
<!--      <div class="event-title short-title">-->
<!--        Ceci est un titre tout à fait normal-->
<!--      </div>-->
<!--    </div>-->
    <p class="short-title">Retrouvez toute l'actualité d'E.péri&school</p>
    <router-link to="/news">
      <button class="bouton-vert">
        Actualités
      </button>
    </router-link>
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
          <li v-b-modal.modal-prevent-closing>
            <p class="lien">Nous Contacter</p>
          </li>
        </ul>
      </div>
    </footer>

  </div>
</template>

<script>
import param from "@/param/param.js";

export default {
  name: 'Home',
  data() {
    return {
      liste_medias:[],
    }
  },
  created(){
    //Liste des mots-clés
    // eslint-disable-next-line no-undef
    axios.get(param.host+"medias")
        .then(response=>{
          console.log("Response", response);
          this.liste_medias = response.data
        })
        .catch(error => console.log(error))
  }
}
</script>
