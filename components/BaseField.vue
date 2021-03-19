<template>
    <div class="field">
        <label class="label"><slot name="label"></slot></label>
        <div class="control has-icons-left"><slot name="input"></slot> </div>
    </div>
</template>

<script>
    export default {
        name: "BaseField"
    }
</script>

<style scoped>

</style>
