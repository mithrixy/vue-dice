<template>
    <div>
        <h3>{{ diceThrow }}</h3>
    
        <button @click="emitEvent">Roll Dice!</button>
    </div>
</template>

<script setup>
defineProps({
    diceThrow: 'some number!'
});

const emit = defineEmits(['updateDice']);

const emitEvent = () => {
    emit('updateDice', '{{ diceResult }}');
}
</script>