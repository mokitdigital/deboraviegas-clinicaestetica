<template>
  <b-card
    class="card"
  >
    <NuxtLink :to="to">
      <b-row>
        <b-col cols="2" class="d-flex justify-content-center align-items-center">
          <b-img
            :src="require(`~/assets/images/${image}.png`)"
            width="50"
          ></b-img>
        </b-col>
        <b-col>
          {{ text }}
        </b-col>
      </b-row>
    </NuxtLink>
  </b-card>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      required: true
    },
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
