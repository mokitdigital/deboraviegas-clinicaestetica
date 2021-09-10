<template>
  <div class="main">
    <header class="d-flex justify-content-center">
      <Header
        :text="'Para entrar em contato conosco, basta clicar nos botões abaixo, de acordo com seu interesse:'"
        :to="'false'"
       />
    </header>

    <article
      v-for="(box, idx) in boxes"
      :key="idx"
      class="d-flex justify-content-center my-5 mx-2"
    >
      <c-card
        :image="box.image"
        :to="box.to"
        :text="box.text"
      />
    </article>

    <footer
      class="d-flex justify-content-center align-items-center bg-light"
      style="height: 50px;"
    >
      <p style="color: #00000080">
        Mokit Digital &copy; 2021 | New websites templates
      </p>
    </footer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      boxes: [
        {
          image: 'whats',
          to: '/whatsapp',
          text: 'Agendamento de Horários'
        },
        {
          image: 'services',
          to: '/procedimentos',
          text: 'Conheça nossos procedimentos'
        },
        {
          image: 'social',
          to: '/redes-sociais',
          text: 'Entre em minhas redes sociais'
        },
        {
          image: 'parcerias',
          to: '/parcerias',
          text: 'Parceiros'
        }
      ]
    }
  }
}
</script>
