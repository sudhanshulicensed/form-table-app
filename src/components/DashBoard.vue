<template>
    <div class="dashboard">
        <div class="form-container">
            <form class="form" v-on:submit.prevent>
                <div class="form-email">
                    <label for="form-email" class="form-in">Your Email</label>
                    <input v-model="email" type="email" id="form-email" class="form-in">
                </div>
                <div class="form-name">
                    <label for="user-name" class="form-in">Your Name</label>
                    <input v-model="name" type="text" id="user-name" class="form-in">
                </div>
                <div class="form-password">
                    <label for="form-password" class="form-in">Password</label>
                    <input v-model="password" type="password" id="form-password" class="form-in">
                </div>
                <!-- <div class="form-password">
                    <label for="form-password" class="form-in">Confirm Password</label>
                    <input type="password" id="form-confirm-password" class="form-in">
                </div> -->
                <div class="form-date">
                    <label for="date-select" class="form-in">Date of birth</label>
                <input v-model="date" type="date" name="date-of-birth" id="date-select" class="form-in">
                </div>
                <div class="checkbox">
                    <input type="checkbox" name="Confirmation" id="condition" class="form-in">
                <label for="condition" class="form-in">Approve Terms and Conditions</label>
                </div>
            </form>
        </div>
        <div class="add-user-btn">
            <p @click="addUserData" >Add User</p>
        </div>
        <DetailTable :userObject="userData" />
    </div>
</template>

<script>

import DetailTable from "./Table/UserDetailTable.vue"

export default {
    name: "DashBoard",
    components: {
        DetailTable
    },
    data(){
        return {
            email: "",
            name: "",
            password: "",
            date: "",
            userData: [],
        }
    },
    methods: {
        addUserForm() {
            console.log("User Clicked");
        },

        addUserData() {
            console.log("Pushing");
            if(this.email && this.name && this.password && this.date) {
                this.userData.push({
                    eMail: this.email,
                    nAme: this.name,
                    pAssword: this.password,
                    dAte: this.date,
                })
                console.log(this.userData);
                console.log("Pushed");
            }
            this.email = "";
            this.name = "";
            this.password = "";
            this.date = "";

        }
    }
}
</script>

<style>
    .dashboard{
        display: flex;
        justify-content: space-between;
        column-gap: 10px;
        align-content: center;
        align-items: center;
        width: 100%;
        margin: 20px auto;
    }

    .add-user-btn p{
        color: #fff;
        font-family: sans-serif;
        box-sizing: border-box;
        padding: 5px 10px;
        border: 2px solid #fff;
        border-radius: 4px;
        cursor: pointer;
    }

    .form{
        display: flex;
        flex-direction: column;
        row-gap: 10px;
    }

    .form-in{
        display: block;
    }
</style>