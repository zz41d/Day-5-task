<template>
    <button>{{ text }} </button>
</template>

<script setup>
  const props= defineProps({
    text:{
    type:String,
    default:'no text specified'
     }
  })

</script>