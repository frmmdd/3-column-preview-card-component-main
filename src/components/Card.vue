<script setup>
  
  defineProps({
    icon: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  })
  
</script>

<template>
  <div class="card">
    <img :src="icon" alt="icon-car" />
    <div class="wraper">
      <h1>{{title}}</h1>
      <p>{{content}}</p>
      <a class="button" href="#">Learn More</a>
    </div>
  </div>
</template>

<style scoped>

  .card {
    max-width: 240px;
    height: -webkit-fill-available;
    padding: 3.5em 2em;
  }

  .wraper {
    height: -webkit-fill-available;
    display: flex;
    flex-direction: column;
    gap: 5em;
    padding: 2em 0 1em 0;
  }

  .button {
    width: fit-content;
    color: inherit !important;
    background: hsl(0, 0%, 95%);
    padding: 0.7em 1em;
    border-radius: 100px;
    text-decoration: none;
  }
  
</style>
