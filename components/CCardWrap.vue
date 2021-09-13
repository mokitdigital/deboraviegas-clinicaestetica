<template>
  <b-row class="d-flex justify-content-center align-items-center p-5">
    <b-col
      xl="4"
      lg="4"
      md="6"
      sm="12"
      class="d-flex justify-content-center align-items-center"
    >
      <a class="card-social card-social--facebook card-social--animate-up">
        <div class="card-social__front">
          <font-awesome-icon
            :icon="faTiktok"
            class="card-social__icon fa fa-facebook"
          />
          <!-- <div class="card-social__data">13 K</div> -->
        </div>

        <div class="card-social__back">
          <div class="card-social__action" @click="openTiktok()">Curta</div>
        </div>
      </a>
    </b-col>
    <b-col
      xl="4"
      lg="4"
      md="6"
      sm="12"
      class="d-flex justify-content-center align-items-center"
    >
      <a class="card-social card-social--instagram card-social--animate-up">
        <div class="card-social__front">
          <font-awesome-icon
            :icon="faInstagram"
            class="card-social__icon fa fa-instagram"
          />
          <!-- <div class="card-social__data">11 K</div> -->
        </div>

        <div class="card-social__back">
          <div class="card-social__action" @click="openInstagram">Siga-me</div>
        </div>
      </a>
    </b-col>
  </b-row>
</template>

<script>
import {
  faTwitter,
  faInstagram,
  faTiktok,
} from '@fortawesome/free-brands-svg-icons'
export default {
  computed: {
    faTiktok() {
      return faTiktok
    },
    faTwitter() {
      return faTwitter
    },
    faInstagram() {
      return faInstagram
    },
  },
  methods: {
    openFacebook() {
      window.location.href = 'http://facebook.com'
    },
    openInstagram() {
      window.location.href = 'http://instagram.com'
    },
    openTwitter() {
      window.location.href = 'http://twitter.com'
    },
  },
}
</script>
