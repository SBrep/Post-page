<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'my-button',
}
</script>

<style scoped>

.btn {
    padding: 10px 15px;
    background: none;
    color: black;
    border: 1px solid black
}
.btn:hover {
    color: black;
    background: rgba(0, 0, 0, 0.1);
}
</style>