<template>
  <div style="padding: 1rem" class="bg-light" >
    <div class="card-columns">
      <app-portfolio-item-card v-for="card in cards" :key="card.id" :info="card.id"></app-portfolio-item-card>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import appPortfolioItemCard from '@/components/PortfolioItemCard.vue'

export default {
  name: 'Home',
  components: {
    appPortfolioItemCard
  },
  data() {
    return {
      cards: [{id:1},{id:2},{id:3},{id:4},{id:5},{id:6},{id:7},{id:8}]
    }
  },
}
</script>


<style scoped>

@media (max-width: 767.98px) {
    .card-columns {
    column-count: 2;
  }
}

@media (max-width: 575.98px) {
    .card-columns {
    column-count: 1;
  }
}



</style>
