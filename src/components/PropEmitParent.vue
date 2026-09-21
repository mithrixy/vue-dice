<template>
    <PropEmitChild  @updateDice="handleDice"/>
    <p>Dice result: {{ diceThrow }}</p>
</template>

<script setup>
import PropEmitChild from './PropEmitChild.vue';
import { ref } from 'vue';

const diceThrow = ref('');

const handleDice = (newDiceThrow) => {
    diceThrow.value = newDiceThrow
}

</script>