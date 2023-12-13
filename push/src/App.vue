<script setup>

import { ref } from 'vue';

let varRef = ref("")

let objeto = ref([{
  name: 'Santiago'
},
{name: 'Simon'}
])

function push () {

 objeto.value.push({name:varRef.value})

}
</script>

<template>
  
<div>
  <div v-for="(obj, index) in objeto" :key="index">{{ obj.name }}</div>
</div>

<div> <input @keypress.enter="push()" v-model="varRef" type="text"> </div>
</template>

<style scoped>

</style>
