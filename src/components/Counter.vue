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
                this.$emit('increase-result');
            },

            decrease() {
                this.count = this.count - 1;
                this.$emit('decrease-result');
            }
        }
    }
</script>

<style scoped>

</style>
