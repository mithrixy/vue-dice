<script setup>
const count = { n };

methods: {
    rollDice() {
    for (let i = 0; i < 8; i++){
        const roll = Math.floor(Math.random() * 6) + 1;
         this.count[roll] = count[roll] + 1;
    }

    for (let i = 0; i < update.length; i++) {
        update[i].textContent = count[i + 1];
    }
}} 

</script>

<template>
    <h3>---Dice---</h3>

    <button @click="rollDice">Throw!</button>
    
    <table>
        <tr>
            <th> Number </th>
            <th> Count </th>
        </tr>
        <tr v-for="n in 6" :key="n">
            <th> {{ n }} </th>
            <th> {{ count n }} </th>
        </tr>
    </table>

</template>

