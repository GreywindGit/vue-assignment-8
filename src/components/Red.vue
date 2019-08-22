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
        color: darkred;
        border: 1px solid red;
        background-color: lightcoral;
        padding: 30px;
        margin: 20px auto;
        text-align: center
    }
</style>