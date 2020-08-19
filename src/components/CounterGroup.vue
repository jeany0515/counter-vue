<template>
    <div class="counter-group">
        <input v-model.number="countNumber" type="number">
        <span>total: {{total}}</span>
        <Counter v-for="(value, index) in counters" v-bind:key="index" @increase-result="increaseResult" @decrease-result="decreaseResult"></Counter>
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
                total: 0
            }
        },
        computed: {
            counters: function () {
                const countNumber = this.countNumber === '' ? 0 : this.countNumber;
                return new Array(countNumber).fill('');
            }
        },
        methods: {
            increaseResult() {
                this.total = this.total + 1;
            },

            decreaseResult() {
                this.total = this.total - 1;
            }
        }
    }
</script>
