<template>
    <footer class="footer">
        <p>© {{ new Date().getFullYear() }} Vinicius Silva</p>
    </footer>
    </template>

    <style lang="scss" scoped>
    @use '../assets/styles/variables' as *;
    @use '../assets/styles/mixins' as *;

    .footer {
    text-align: center;
    padding: $spacing-md;
    background-color: $color-background-alt;
    color: $color-primary;
    }
</style>

