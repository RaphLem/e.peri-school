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
          <b-dropdown id="dropdown-form" text="---------" ref="dropdown" size="sm">
            <b-dropdown-form>
              <b-button size="sm" @click="filter">Filtrer</b-button>
            </b-dropdown-form>
          </b-dropdown>
        </div>
      </div>
      <div id="filter">
        <p>Filtrer par</p>
        <div>
          <b-dropdown id="dropdown-form" text="---------" ref="dropdown" size="sm">
            <b-dropdown-form>
              <b-form-checkbox value="mot" class="mb-3">mot</b-form-checkbox>
              <b-button size="sm" @click="filter">Filtrer</b-button>
            </b-dropdown-form>
          </b-dropdown>
        </div>
      </div>
    </div>
    <div class="event-card">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
      <div class="event-grid">
        <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur doloremque eligendi, harum in incidunt
          mollitia.</p></div>
    </div>
    <div class="event-card">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
      <div class="event-grid">
        <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur doloremque eligendi, harum in incidunt
          mollitia.</p></div>
    </div>
    <div class="event-card">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
      <div class="event-grid">
        <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur doloremque eligendi, harum in incidunt
          mollitia.</p></div>
    </div>
    <div class="event-card">
      <div class="event-title short-title">
        Ceci est un titre tout à fait normal
      </div>
      <div class="event-grid">
        <img class="event-image" src="@/assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequuntur doloremque eligendi, harum in incidunt
          mollitia.</p></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "News",
  data() {
    return {
      selected: [], // Must be an array reference!
      options: []
    }
  },
  methods: {
    filter() {
      this.$refs.dropdown.hide(true)
    }
  }
}
</script>

<style scoped>

</style>