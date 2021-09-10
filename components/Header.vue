<!-- Please remove this file from your project -->
<template>
  <b-card
    class="card"
  >
    <b-row>
      <b-col cols="4" class="d-flex justify-content-center align-items-center">
        <div
          style="width: 100px; margin: 50px;"
        >
          <b-img
            src="~/assets/images/logotipo.png"
            style="max-width: 100px; border-radius: 50%; box-shadow: 4px 4px 9px 5px rgba(0,0,0,0.2);"
          ></b-img>
        </div>
      </b-col>
      <b-col>
        <b-row>
          <b-col cols="12" class="box-title">
            <h1 class="title">
              Débora Viegas
            </h1>
            <span>Clínica Estética</span>
          </b-col>
          <b-col cols="12">
            <p>
              {{ text }}
            </p>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row v-if="to !== 'false'">
      <b-col>
        <NuxtLink :to="to">
          Voltar
        </NuxtLink>
      </b-col>
    </b-row>
  </b-card>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    },
    to: {
      type: String,
      required: true
    }
  }
}
</script>
