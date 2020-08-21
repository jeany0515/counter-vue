<template>
    <div class="counter-group">
        <input v-model.number="countNumber" type="number">
        <span>total: {{total}}</span>
        <Counter v-for="(value, index) in counters" v-bind:key="index"></Counter>
    </div>
</template>

<script>
    import Counter from "./Counter";
    export default {
        name: 'CounterGroup',
        components: {
            Counter
        },
        data() {
            return {
                countNumber: 0,
            }
        },
        computed: {
            counters() {
                const countNumber = this.countNumber === '' ? 0 : this.countNumber;
                return new Array(countNumber).fill('');
            },
            total() {return this.$store.state.total}
        }
    }
</script>
