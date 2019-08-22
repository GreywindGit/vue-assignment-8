<template>
    <div>
        <slot name="title"></slot>
        <slot name="artist"></slot>
    </div>
</template>

<script>

</script>

<style scoped>
    div {
        color: darkgreen;
        border: 1px solid green;
        background-color: lightgreen;
        padding: 30px;
        margin: 20px auto;
        text-align: center
    }
</style>