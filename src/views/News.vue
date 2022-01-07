<template>
  <div id="news">
    <div id="news-heading">
      <img class="background-home" src="@/assets/img/picture/E-Perischool10Nov20TIML0150.jpg"
           alt="">
      <div id="black-filter"></div>
      <h1>Actualités</h1>
      <h2>Découvrez toutes les news d'E.péri&school</h2>
    </div>
    <div id="search-menu">
      <div id="sort">
        <p>Trier par</p>
        <div>
          <b-dropdown id="dropdown-form" text="-----------" ref="dropdown" size="sm">
            <b-dropdown-item href="#">Le plus récent</b-dropdown-item>
            <b-dropdown-item href="#">Le plus ancien</b-dropdown-item>
            <b-dropdown-item href="#">Ordre alphabétique</b-dropdown-item>
          </b-dropdown>
        </div>
      </div>
      <div id="filter">
        <p>Filtrer par</p>
        <div>
          <b-dropdown text="-----------" ref="dropdown" size="8">
            <b-dropdown-form>
              <b-form-checkbox v-for="keywords in keywords" value="mot" id="checkbox" class="mb-3" :key="keywords.id">
                {{keywords.title.rendered}}
              </b-form-checkbox>
              <b-button size="sm">Filtrer</b-button>
            </b-dropdown-form>
            <form action=""></form>
          </b-dropdown>
        </div>
      </div>
    </div>
    <div>
      <router-link to="/articles" id="card-grid" style=".lien{display: contents;
        color: #000;text-decoration: none;} ">
        <div v-for="media in liste_medias" :key="media.id" class="event-card">
          <div class="event-title short-title">
            {{ media.acf.label }}
          </div>

          <div class="event-grid">
            <img class="event-image" :src=media.acf.file.url alt="">
            <p>{{ media.acf.description }}</p>
          </div>
        </div>
      </router-link>

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
      keywords: [],
      liste_medias: [],
    }
  },
  created() {
    //Liste des mots-clés
    // eslint-disable-next-line no-undef
    axios.get(param.host + "keywords")
        .then(response => {
          console.log("Response", response);
          this.keywords = response.data
        })
        .catch(error => console.log(error))

    // eslint-disable-next-line no-undef
    axios.get(param.host + "medias")
        .then(response => {
          console.log("Response", response);
          this.liste_medias = response.data
        })
        .catch(error => console.log(error))
  }
}
</script>

<style scoped>

</style>