<template>
    <div class="counter">
        <button @click="increase()">+</button>
        <span>{{count}}</span>
        <button @click="decrease()">-</button>
    </div>
</template>

<script>
    export default {
        name: 'Counter',
        data() {
            return {
                count: 0
            }
        },
        methods: {
            increase() {
                this.count = this.count + 1;
            },

            decrease() {
                this.count = this.count - 1;
            }
        }
    }
</script>

<style scoped>

</style>
