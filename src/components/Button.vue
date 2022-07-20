<script setup>
defineProps({
    primary: {
        type: Boolean,
        required: false,
        default: false
    }
})
</script>

<template>
    <button :class="{ primary }">
        <slot />
    </button>
</template>

<style>
button {
    display: flex;
    align-items: center;
    height: 48px;
    background: #ffffff;
    border: 1px solid #e1e3e6;
    box-shadow: 0px 4px 2px -2px rgba(27, 46, 94, 0.02);
    border-radius: 8px;
    padding: 0 19px;
}

button.primary {
    background: linear-gradient(180deg, #6989FE 0%, #3C64F4 100%);
    color: #FFFFFF;
    font-weight: bold;
    box-shadow: none;
    border: none;
}

button.secondary {
    background: rebeccapurple;
    color: #FFFFFF;
    font-weight: bold;
    box-shadow: none;
    border: none;
}
</style>