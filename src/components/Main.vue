<template>
  <main>
    <div class="container-fluid p-5">
      <div class="row d-flex  gap">
          <Card
          v-for="(film, index) in cards.film"
          :key="index"
          :arname="film"
          />
          <Card
          v-for="(serie, index) in cards.series"
          :key="index"
          :arname="serie"
          />
        </div>
    </div>
  </main>
</template>

<script>
import Card from './Card.vue';
export default {
    name: 'Main',
    components:{
        Card,
    },
    props: {
    cards: Array,
    },
}
</script>
<style lang="scss">
  main{
    background-color: #141414;
    .gap{
      justify-content: space-between;
      gap: 60px;
      margin: 0 auto;
    }
  }
</style>