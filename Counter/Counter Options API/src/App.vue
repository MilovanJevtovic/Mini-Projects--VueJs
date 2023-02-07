<script>

  export default {
    data(){
      return{
        count: 0,
      };
    },

    methods:{
      colorChanger(){
        if(this.count < 0){
          return "red";
        }else if(this.count > 0){
          return "blue"
        }
      },
      addCount(){
        this.count++;
      },
      subCount(){
        this.count--;
      },
      resetCount(){
        this.count = 0;
      },

    }

  }

</script>

<template>
  <main>
    <h1>Counter</h1>
    <h2
    :style="{color: colorChanger()}"
    >{{ count }}</h2>
    <div>
      <button @click="subCount()">DECREASE</button>
      <button @click="resetCount()">RESET</button>
      <button @click="addCount()">INCREASE</button>
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

  h1{
    color: #102A42;
    font-size: 70px;
    margin: 0px;
  }

  h2{
    margin: 10px 0px;
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