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
            add: function() {
                this.number++;
                this.$emit("addToParent", this.number)
            },
            decrease: function() {
                this.number--;
                this.$emit("decreaseToParent", this.number)
            }
        }
    }
</script>

<style>

</style>