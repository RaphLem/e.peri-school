<template>
  <div id="mentions">
    <div id="mentions-heading">
      <img class="background-home" src="@/assets/img/picture/E-Perischool10Nov20TIML0150.jpg"
           alt="">
      <div id="black-filter"></div>
      <h1>{{media.acf.label}}</h1>
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
          <li v-b-modal.modal-prevent-closing>
            <p class="lien">Nous Contacter</p>
          </li>
        </ul>
      </div>
    </footer>
</div>

</template>

<script>
import param from "@/param/param"

export default {
  name: "News",
  data() {
    return {
      liste_medias: [],
    }
  },
  created() {
    // eslint-disable-next-line no-undef
    axios.get(param.host + "medias")
        .then(response => {
          console.log("Response", response);
          this.liste_medias = response.data
        })
        .catch(error => console.log(error))
  },
}
</script>

<style scoped>

</style>