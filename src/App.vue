<template>
  <div id="app">
    <DashBoard />
  </div>
</template>

<script>

import DashBoard from "./components/DashBoard.vue"

export default {
  name: 'App',
  components: {
    DashBoard,
  },
  data(){
    return {

    }
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }

  #app{
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    justify-content: center;
    align-items: center;
    align-content: center;
    width: 50%;
    margin-right: auto;
    margin-left: auto;
    margin-top: 50px;
    padding: 20px;
    background-color: #FBAB7E;
    background-image: linear-gradient(62deg, #FBAB7E 0%, #F7CE68 100%);
  }
</style>
