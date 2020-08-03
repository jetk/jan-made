<template>
  <div style="padding: 1rem" class="bg-dark" >
    <div class="row justify-content-center">
      <app-portfolio-item v-for="card in cards" :key="card.displayName" :info="card.displayName" :cardData ="card"></app-portfolio-item>
    </div>
  </div>
</template>

<script>
import {portfolio} from '@/itemIndex.js'

// @ is an alias to /src
import appPortfolioItem from '@/components/PortfolioItem.vue'

export default {
  name: 'Home',
  components: {
    appPortfolioItem
  },
  data() {
    return {
      cards: portfolio
    }
  },
}
</script>


<style scoped>
/* 
@media (max-width: 767.98px) {
    .card-columns {
    column-count: 2;
  }
}

@media (max-width: 575.98px) {
    .card-columns {
    column-count: 1;
  }
} */



</style>
