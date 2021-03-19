<template>

    <div class="container">
        <div class="columns is-centered">
            <div class="column is-7-tablet is-6-desktop is-5-widescreen">
                <slot></slot>
            </div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "BasePage"
    }
</script>

<style scoped>

</style>
