<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.btn {
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
    cursor: pointer;
}

.btn:hover{
    color: rgb(3, 87, 87);
    border: 1px solid rgb(3, 87, 87);
}
</style>