<script setup>
defineProps(['title'])
defineEmits(['emits'])
</script>

<template>

  <ul>
  <li>{{title}}</li>
  </ul>
  	<button @click="$emit('enlarge-text')">Enlarge text</button>
</template>