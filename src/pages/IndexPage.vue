<template>
  <q-page class="flex flex-center text-brown">
    <div class="row">
      <q-input 
      v-model="data.name"
      input-class="text-center text-brown text-h6" 
      outlined
      label="Name"
      color="teal"
      filled />
    </div>
   <div class="row full-width items-center">
    <div class="col text-center">
      <q-btn 
      @click="decreaseCounter"
      round 
      size="xl"
      icon="remove" 
      />
    </div>
    <div class="col text-center text-h1">
      {{ data.counter }}
    </div>
    <div class="col text-center">
      <q-btn 
      @click="increaseCounter"
      round 
      size="xl"
      icon="add" 
      />
    </div>
   </div>
   <div class="row">
      <q-btn 
      @click="resetCounter"
      round 
      size="xl"
      icon="restart_alt" 
      />
    </div>
  </q-page>
</template>

<style>
.q-page{
  max-width: 700px;
  margin: 0 auto;

}
</style>


<script setup>

  import { reactive } from 'vue';

const data = reactive({
  counter: 0,
  name: ''
})

const increaseCounter = () =>{
  data.counter++
}

const decreaseCounter = () =>{
  if (data.counter > 0) {
    data.counter--
  }
}
const resetCounter = () =>{
  data.counter = 0
}


</script>
