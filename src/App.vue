<template>
  <div id="app">
    <AddDetail />
    <EditDetail />
  </div>
</template>

<script>

import AddDetail from "./components/AddDetails.vue"
import EditDetail from "./components/EditDetails.vue"

export default {
  name: 'App',
  components: {
    AddDetail,
    EditDetail,
  }
}
</script>

<style>

</style>
