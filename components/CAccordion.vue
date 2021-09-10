<template>
  <b-card
    class="card"
    @click="openAccordion"
  >
    <h3>
      {{ title }}
    </h3>
  

    <b-collapse
      :id="toggle"
      accordion="my-accordion"
      role="tabpanel"
      style="width: 100%; flex-grow: 1; flex-basis: 100%;"
    >
      <b-card-body class="d-flex flex-wrap">
        <b-card-text>{{ text }}</b-card-text>
        <div class="break"></div>
        <b-card-text>R${{ value }},00</b-card-text>
        <b-card-text class="ml-auto">
          <b-button
            class="btn-contact"
            @click="openWhatsapp(title)"
          >
            Entrar em contato
          </b-button>
        </b-card-text>
      </b-card-body>
    </b-collapse>
  </b-card>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    toggle: {
      type: String,
      required: true,
    },
    value: {
      type: String,
      required: true,
    }
  },
  methods: {
    openAccordion () {
      this.$root.$emit(`bv::toggle::collapse`, this.toggle)
    },
    openWhatsapp (text) {
      const question = "Olá! Estava navegando em seu site e gostaria de saber mais sobre o procedimento de "

      text = text.replace(' ', '%20')

      window.location.href = `https://wa.me/555183283937?text=${question}${text}.`
    }
  }
}
</script>