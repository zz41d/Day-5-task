<script setup>
import { ref } from 'vue'
import BlogPost from './components/BlogPost.vue'
import MyButton from './components/MyButton.vue';

// const header=ref('Welcome to Components')
const adv =ref('Advance Vue Concepts')

const headingClick= ()=>{
    adv.value= 'Props and Emits'
}




const posts = ref([
  { id: 1, title: 'With defineProps' },
  { id: 2, title: 'I am able to pass the data to components' },
  { id: 3, title: 'via custom attributes' }
])
const fontSize=ref(1)
</script>

<template> 
<div class="all">
 <h1 @click="headingClick" >Welcome to {{ adv }} 
   <!-- <p v-if="headingClick=click+1">{{ adv }}</p> -->
</h1>
<div :style="{ fontSize: fontSize + 'em' }">

	<BlogPost
  	v-for="post in posts"
	  :key="post.id"
  	:title="post.title"
		 @enlarge-text="fontSize += 0.1"
	></BlogPost>
</div>

 <MyButton text="MyButton text"/>
 
</div>
</template>
<style scoped>
.all{
  display: block;
}
</style>