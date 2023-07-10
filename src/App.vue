<script setup>
  import Card from "./components/Card.vue"
</script>

<template>
  <main>
    <div class="container">
      <Card v-for="card in cards"
        :style="{ 
          background: card.color,
          color: card.color
        }"
        :icon="card.icon"
        :title="card.title"
        :content="card.content"
      />
    </div>
  </main>
</template>

<script>
import { cards } from "./data.js"
  
  export default {
    data () {
      return {
        cards: cards
      }
    },
  }
  
</script>


<style scoped>
  
  .container {
    display: grid;
    grid-template-rows: auto;
  }

  @media screen and (min-width: 490px) {
    .container {
      grid-template-columns: repeat(2, 240px);
    }
  }

  @media screen and (min-width: 750px) {
    .container {
      grid-template-columns: repeat(3, 240px);
    }
  }
  
</style>
