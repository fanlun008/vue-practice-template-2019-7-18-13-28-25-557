<template>
 <div>
    <!-- <span>{{this.counterNum}}</span> -->
    <calc v-for="count in this.counterNum" :key="count"
            v-on:addToParent="addToParent" v-on:decreaseToParent="decreaseToParent"
    ></calc><br/>
    <span>total: {{this.totalCount}}</span>
 </div>
</template>

<script>
    import calc from './calc.vue';
    export default {
        components: {
            calc
        },
        props: ["counterNum"],
        data: function() {
            return {
                totalCount: 0
            }
        },
        methods: {
            addToParent: function(data) {
                // this.totalCount++;
                this.totalCount = this.totalCount + data
            },
            decreaseToParent: function(data) {
                this.totalCount = this.totalCount - data
            }
        },
        watch: {
            counterNum: function() {
                this.totalCount = 0
            }
        }
    }
</script>

<style>

</style>