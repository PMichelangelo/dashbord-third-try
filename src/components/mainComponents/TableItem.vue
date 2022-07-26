<script setup>
const props = defineProps({
    icon: {
        type: String,
        required: true
    },
    name: {
        type: String,
        required: true,
    },
    email: {
        type: String,
        required: true
    },
    status: {
        type: String,
        required: true
    },
    role: {
        type: String,
        required: true
    }

})

</script>

<template>
    <tr>
        <td> <img :src="props.icon"> <span>{{ props.name }}</span></td>
        <td>{{ props.email }}</td>
        <td>{{ props.status }}</td>
        <td>{{ props.role }}</td>
    </tr>
</template>

<style scoped>
td {
    padding: 20px 24px;
    gap: 16px;
    color: #5A6474;
}

td:nth-child(1) {
    font-weight: 500;
    font-size: 18px;
    line-height: 24px;
    color: #5A6474;
}

img {
    width: 32px;
    height: 32px;
    border-radius: 99px;
}
</style>