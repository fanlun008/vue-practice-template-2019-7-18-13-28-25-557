<template>
 <div>
     <div>
         <button @click="add">+</button>
         <input type="text" v-model="number">
         <button @click="decrease">-</button>
     </div>
 </div>
</template>

<script>
    export default {
        data() {
            return {
                number: 0
            }
        },
        methods: {
            add(){
                this.number++;
            },
            decrease() {
                this.number--;
            }
        }
    }
</script>

<style>

</style>