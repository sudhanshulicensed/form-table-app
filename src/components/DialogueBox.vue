<template>
    <div class="diag-box">
        <div class="diag-content">
            <p>Do you confirm ?</p>
        </div>
        <div class="diag-btn">
            <CancelButton />
            <ConfirmButton />
        </div>
    </div>
</template>

<script>

import CancelButton from "./Buttons/Cancelbtn.vue"
import ConfirmButton from "./Buttons/Confirmbtn.vue"

export default {
    name: "DialogueBox",
    components: {
        CancelButton,
        ConfirmButton,
    }
}
</script>

<style>
   .diag-box{
       display: flex;
       flex-direction: column;
       /* display: grid;
       grid-template-rows: 1fr 1fr;
       grid-template-columns: 1fr; */
       width: 200px;
       height: 100px;
       border: 2px solid coral;
       border-radius: 4px;
   }

   .diag-content{
       height: 40%;
       text-align: center;
       /* grid-column-start: 1;
       grid-column-end: -1;
       grid-row-start: 1;
       grid-row-end: 2; */
   }

   .diag-btn{
       height: 60%;
       display: flex;
       justify-content: space-evenly;
       /* background-color: aqua; */
       /* grid-column-start: 1;
       grid-column-end: -1;
       grid-row-start: 2;
       grid-row-end: 3; */
   }
</style>