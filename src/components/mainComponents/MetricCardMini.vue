<script setup>

import caretIcon from "../../assets/icons/caret-arrow-up.svg"

const props = defineProps({
    label: {
        type: String,
        required: true,
    },
    price: {
        type: String,
        required: true,
    },
    down: {
        type: Boolean,
        default: false
    }
})
</script>

<template>
    <div class="wrapper">
        <div class="label">
            <p>{{ props.label }}</p>
            <img :src="caretIcon" :class="{ down: props.down }" class="icon" />
        </div>
        <h2> {{ props.price }}</h2>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 24px 16px;
    gap: 4px;
    height: 144px;
    min-width: 236px;
    background: #F8F8F8;
    border-radius: 8px;
    white-space: nowrap;
}

.icon.down {
    transform: rotate(180deg);
}

.label {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 0px;
    gap: 4px;
    height: 24px;
}

p {
    font-weight: 400;
    font-size: 18px;
    line-height: 24px;
    color: #757D8A;
}

h2 {
    font-weight: 700;
    font-size: 24px;
    line-height: 32px;
    color: #404D61;
}

.wrapper:hover {
    background: linear-gradient(180deg, #6989FE 0%, #3C64F4 100%);

}

.wrapper:hover h2 {
    color: white;
}

.wrapper:hover p {
    color: white;
}
</style>