<template>
    <div class="edit-user-form">
        <form>
            <div class="edit-email">
                <label for="ed-email">New Email</label>
                <input v-model="email" type="email" id="ed-email">
            </div>
            <div class="edit-name">
                <label for="ed-name">New Name</label>
                <input v-model="name" type="text" id="ed-name">
            </div>
            <div class="edit-user-btn">
            <p @click="editUserData" >Edit User</p>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    name: "EditUserForm",
    data() {
        return {
            email: "",
            name: "",
        }
    },
    methods: {
        
    }
}
</script>

<style>

</style>