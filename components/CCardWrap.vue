<template>
  <div>
    <div class="card-wrap flex-wrap">
      <a
        class="card-social card-social--facebook card-social--animate-up"
      >
        <div class="card-social__front">
          <font-awesome-icon
            :icon="faFacebook"
            class="card-social__icon fa fa-facebook"
          />
          <div class="card-social__data">13 K</div>
        </div>

        <div class="card-social__back">
          <div class="card-social__action" @click="openFacebook()">Curta</div>
        </div>
      </a>

      <a
        class="card-social card-social--twitter card-social--animate-up"
      >
        <div class="card-social__front">
          <font-awesome-icon
            :icon="faTwitter"
            class="card-social__icon fa fa-twitter"
          />
          <div class="card-social__data">10.5 K</div>
        </div>

        <div class="card-social__back">
          <div class="card-social__action" @click="openTwitter">Siga-me</div>
        </div>
      </a>

      <a
        class="
          card-social card-social--instagram card-social--animate-up
        "
      >
        <div class="card-social__front">
          <font-awesome-icon
            :icon="faInstagram"
            class="card-social__icon fa fa-instagram"
          />
          <div class="card-social__data">11 K</div>
        </div>

        <div class="card-social__back">
          <div class="card-social__action" @click="openInstagram">Siga-me</div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import {
  faFacebook,
  faTwitter,
  faInstagram,
} from '@fortawesome/free-brands-svg-icons'
export default {
  computed: {
    faFacebook() {
      return faFacebook
    },
    faTwitter() {
      return faTwitter
    },
    faInstagram() {
      return faInstagram
    },
  },
  methods: {
    openFacebook () {
      window.location.href = 'http://facebook.com'
    },
    openInstagram () {
      window.location.href = 'http://instagram.com'
    },
    openTwitter () {
      window.location.href = 'http://twitter.com'
    }
  }
}
</script>
