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
                this.$emit("addToParent", 1)
            },
            decrease: function() {
                this.number--;
                this.$emit("decreaseToParent", 1)
            }
        }
    }
</script>

<style>

</style>