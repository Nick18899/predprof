<template>
    <input
            @input="$emit('update:modelValue', $event.target.value)"
            v-model="age"
            min="25"
            max="150"
            placeholder="Введите вес"
            class="form-control"
    />
</template>

<script>
    export default {
        name: "BaseInput",
    }
</script>

<style scoped>

</style>
