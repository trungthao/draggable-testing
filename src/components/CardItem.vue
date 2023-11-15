<template>
<div class="card-item">{{ content }}</div>
</template>

<script setup>
const props = defineProps(['content']);
</script>

<style scoped>
.card-item {
    width: 50px;
    height: 50px;
    background-color: #fff;
    text-align: center;
    vertical-align: middle;
    border: 1px solid #000;
    margin-top: 20px;
}
</style>