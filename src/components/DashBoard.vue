<template>
    <div class="dashboard">
        <AddUser />
    </div>
</template>

<script>

import AddUser from "./AddUser.vue"

export default {
    name: "DashBoard",
    components: {
        AddUser,
  }
}
</script>

<style>
    .dashboard{
        display: flex;
        justify-content: flex-end;
        align-content: center;
        align-items: center;
        width: 100%;
    }
</style>