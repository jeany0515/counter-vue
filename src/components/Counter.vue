<template>
    <div class="counter">
        <button @click="increase">+</button>
        <span>{{count}}</span>
        <button @click="decrease">-</button>
    </div>
</template>

<script>
    import { mapActions } from 'vuex'
    export default {
        name: 'Counter',
        data() {
            return {
                count: 0
            }
        },
        methods: mapActions([
            'increase',
            'decrease',
        ])
    }
</script>

