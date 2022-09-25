<script setup >
import Hello from './components/HelloWorld.vue'
import Card from './components/Card.vue'


</script>

<template>
  <div class="container mt-5">
    <Hello/>
    <Card 
    :titol="'Exemple de titol'"
    :cos="'lorem ipsum lorem'"
    :peu="'lorem'"
    />
  </div>
</template>
