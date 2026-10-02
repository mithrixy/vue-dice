<script setup>
import { ref } from 'vue'

const count = ref({
    1: 0,
    2: 0,
    3: 0,
    4: 0,
    5: 0,
    6: 0
})

function rollDice() {
    for (let i = 0; i < 8; i++) {
        const roll = Math.floor(Math.random() * 6) + 1
        count.value[roll] = count.value[roll] + 1
    }
}
</script>

<template>
    <h3>--- Dice ---</h3>

    <button @click="rollDice">Throw!</button>

    <table>
        <tr>
            <th>Number</th>
            <th>Count</th>
        </tr>

        <tr v-for="n in 6" :key="n">
            <th>{{ n }}</th>
            <th>{{ count[n] }}</th>
        </tr>
    </table>
</template>


