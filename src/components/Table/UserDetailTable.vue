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
                <td>Edit</td>
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
            console.log(index)
            // this.userObject.splice(index, 1)
        }
    }

}
</script>

<style>
    tr, td, th{
        border: 1px solid black;
    }
</style>