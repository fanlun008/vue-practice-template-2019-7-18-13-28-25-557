<template>
 <div>
    <span>{{this.counterNum}}</span>
    <calc v-for="count in this.counterNum" :key="count"></calc>
 </div>
</template>

<script>
    import calc from './calc.vue';
    export default {
        components: {
            calc
        },
        props: ["counterNum"],
        methods: {
            
        }
    }
</script>

<style>

</style>