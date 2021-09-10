<template>
  <div class="main">
    <header class="d-flex justify-content-center flex-wrap">
      <Header
        :text="'Procure os procedimentos e clique para saber mais sobre'"
        :to="'/'"
      />
    </header>
    
    <article
      v-for="(pd, idx) in proced"
      :key="idx"
      class="d-flex justify-content-center flex-wrap my-3 mx-2 card-article"
      style="overflow-anchor: none;"
    >
      <nav
        class="text-center mx-5 my-4 border-bottom"
      >
        <h2>
          {{ pd.name }}
        </h2>
      </nav>
      <div class="break"></div>
        
      <div class="accordion m-3" role="tablist">
        <b-row>
          <b-col
            v-for="(t, tidx) in pd.types"
            :key="tidx"
            cols="12"
            class="p-0"
          >
            <c-accordion
              :toggle="t.toggle"
              :title="t.title"
              :text="t.text"
              :value="t.value"
              class="my-2"
            />
          </b-col>
        </b-row>
      </div>
    </article>
  </div>
</template>

<script>
import CAccordion from '~/components/CAccordion.vue'
import { proced } from '~/data/procedimentos'
export default {
  components: { CAccordion },
  data () {
    return {
      proced
    }
  }
}
</script>