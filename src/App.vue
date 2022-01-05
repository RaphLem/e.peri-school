<template>
  <div>
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
                  <img class="img-fluid" src="@/assets/img/icons/Icon_black_newspaper.svg" alt="">
                  Actualités
                </router-link>
              </li>
              <li @click="close()">
                <router-link class="lien" to="/about">
                  <img class="img-fluid" src="@/assets/img/icons/Icon_black_info.svg" alt="">
                  À propos
                </router-link>
              </li>
              <li @click="close()" v-b-modal.modal-prevent-closing>
                <img src="@/assets/img/icons/Icon_black_contacts.svg" alt="">
                <p class="lien">Contact</p>
              </li>
            </ul>
          </div>
        </div>
        <div class="nav-bar">
          <div>
            <ul>
              <li>
                <router-link class="lien" to="/news">
                  <img src="@/assets/img/icons/Icon_newspaper.svg" alt="">
                  Actualités
                </router-link>
              </li>
              <li>
                <router-link class="lien" to="/about">
                  <img src="@/assets/img/icons/Icon_info.svg" alt="">
                  À propos
                </router-link>
              </li>
              <li id="item-contact" v-b-modal.modal-prevent-closing>
                <img class="img-fluid" src="@/assets/img/icons/Icon_contacts.svg" alt="">
                <a class="lien">Contact</a>
              </li>
            </ul>
          </div>
        </div>

      </nav>
    </header>
    <router-view/>
    <div id="formulaire">
      <b-modal
          id="modal-prevent-closing"
          ref="modal"
          title="Une question ? Contactez-nous"
          @show="resetModal"
          @hidden="resetModal"
          @ok="handleOk"
      >
        <form ref="form" @submit.stop.prevent="handleSubmit">
          <b-form-group
              label="Name"
              label-for="name-input"
              invalid-feedback="Name is required"
              :state="nameState">
            <b-form-input
                id="name-input"
                v-model="name"
                :state="nameState"
                required
            ></b-form-input>
          </b-form-group>
          <b-form-group
                label="E-mail"
                label-for="email-input"
                invalid-feedback="E-mail is required"
                :state="emailState">
              <b-form-input
                  id="email-input"
                  v-model="email"
                  :state="emailState"
                  required
              ></b-form-input>
          </b-form-group>
        </form>
      </b-modal>
    </div>
  </div>
</template>

<style lang="less">
</style>
<script>

export default {
  name: 'App',
  components: {},
  data() {
    return {
      utilisateur: {
        username: null,
        password: null,
      },
      message: null,
      visible: false,
      name: '',
      email: '',
      nameState: null,
      emailState: null,
    }
  },
  created() {

  },
  methods: {
    close() {
      document.documentElement.classList.remove('menu-open')
    },

    //Formulaire de contact
    checkFormValidity() {
      const valid = this.$refs.form.checkValidity()
      this.nameState = valid
      this.emailState = valid
      return valid
    },
    resetModal() {
      this.name = ''
      this.nameState = null
    },
    handleOk(bvModalEvt) {
      // Prevent modal from closing
      bvModalEvt.preventDefault()
      // Trigger submit handler
      this.handleSubmit()
    },
    handleSubmit() {
      // Exit when the form isn't valid
      if (!this.checkFormValidity()) {
        return
      }
      // Push the name to submitted names
      // Hide the modal manually
      this.$nextTick(() => {
        this.$bvModal.hide('modal-prevent-closing')
      })
    }
  }
}
</script>
<style>
@import "assets/css/styles.css";
@import "assets/css/menu.css";
</style>