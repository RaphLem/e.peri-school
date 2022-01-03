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
    <div class="event-card">
      <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0317.jpg" alt="">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
    </div>
    <div class="event-card">
      <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
    </div>
    <div class="event-card">
      <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0352.jpg" alt="">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
    </div>
    <p class="short-title">Retrouvez toute l'actualité d'E.péri&school</p>
    <router-link to="/news">
      <button class="bouton-vert">
        Actualités
      </button>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>
