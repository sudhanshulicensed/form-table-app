<template>
  <div id="app">
    <DashBoard />
    <DetailTable />
  </div>
</template>

<script>

import DashBoard from "./components/DashBoard.vue"
import DetailTable from "./components/UserDetailTable.vue"

export default {
  name: 'App',
  components: {
    DashBoard,
    DetailTable,
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
    justify-content: center;
    align-items: center;
    align-content: center;
    width: 80%;
    margin-right: auto;
    margin-left: auto;
    background-color: aquamarine;
  }
</style>
