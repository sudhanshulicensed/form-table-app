<template>
    <div class="detail-table">
        <table>
            <tr>
                <th>Email</th>
                <th>Name</th>
                <th>Date of Birth</th>
                <th colspan="2">Edit | Delete</th>
            </tr>
            <tr v-for="(detail, index) in userObject" :key="index">
                <td>{{ detail.eMail }}</td>
                <td>{{ detail.nAme }}</td>
                <td>{{ detail.pAssword }}</td>
                <td @click="editUser(index)">Edit</td>
                <td @click="deleteUser(index)">Delete</td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    name: "DetailTable",
    props: {
        userObject :{
            type: Array,
            default: () => [],
        },
    },
    data() {
        return {
            
        }
    },
    methods: {
        deleteUser(index) {
            this.$emit("del", index)
        },

        editUser(index) {
            this.$emit("edit", index)
        }
    }
}
</script>

<style>
    tr, td, th{
        border: 1px solid black;
    }
</style>