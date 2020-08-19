<template>
    <div class="counter-group">
        <input v-model.number="countNumber" type="number">
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
                countNumber: 0
            }
        },
        computed: {
            counters: function () {
                const countNumber = this.countNumber === '' ? 0 : this.countNumber;
                return new Array(countNumber).fill('');
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
