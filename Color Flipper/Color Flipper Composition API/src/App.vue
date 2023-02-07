<script setup>
  import {ref} from "vue"

  let color = ref("");
  const list = ["red", "blue", "green", "yellow", "brown",
  "orange", "black", "gray", "gold", "purple"];

  function colore(){
    let b = Math.floor(Math.random() * 10)
    color.value = list[b];
  }

</script>

<template>
  <main :style="{backgroundColor:color}">
    <div>
    <h1>Background Color : {{ color }}</h1>
    <button @click="colore()">CLICK ME</button>
    </div>
  </main>
</template>

<style scoped>
  main{
    height: 100vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-content: center;
    justify-content: center;
    text-align: center;
    color: white;
  }

  button{
    font-size: 20px;
    margin: 20px 0px;
    background-color: transparent;
    border: 2px solid white;
    color: white;
    padding: 15px;
    border-radius: 20px;
  }
</style>