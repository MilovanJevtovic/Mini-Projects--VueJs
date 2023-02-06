<script setup>
import {ref} from "vue"

let colore

const counter = ref(0);




</script>

<template>

  <main>
    <h4>Counter</h4>
    <h2
    v-if="counter > 0" style="color:blue"
    >{{ counter }}</h2>
    <h2
    v-else-if="counter < 0" style="color:red"
    >{{counter}}</h2>
    <h2
    v-else
    >{{counter}}</h2>
    <div class="buttons">
      <button @click="counter--">DECREASE</button>
      <button @click="counter = 0">RESET</button>
      <button @click="counter++">INCREASE</button>
    </div>
  </main>
  
</template>

<style scoped>

  main{
    margin: 0px;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #F1F5F8;
  }

  h4{
    color: #102A42;
    font-size: 70px;
    margin: 0px;
  }

  h2{
    margin: 30px 0px;
    font-size: 5rem;
    color: #102A42;
  }

  button{
    margin: 0px 10px;
    padding: 10px;
    letter-spacing: 5px;
    background: transparent;
    border: 2px solid #102A42;
    border-radius: 10px;
    transition: background-color 0.3s, color 0.3s;
  }

  button:hover{
    background-color: #102A42;
    color: #F1F5F8;
  }

</style>