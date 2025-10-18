<template>
    <nav class="navbar">
        <div class="logo">
        <router-link to="/">Vinicius Silva</router-link>
        </div>

        <!-- Botão hamburguer -->
        <button class="menu-toggle" @click="toggleMenu">
        <span :class="{ open: isOpen }"></span>
        </button>

        <ul :class="['nav-links', { open: isOpen }]">
        <li><router-link to="/" @click="closeMenu">Início</router-link></li>
        <li><router-link to="/sobre" @click="closeMenu">Sobre</router-link></li>
        <li><router-link to="/projetos" @click="closeMenu">Projetos</router-link></li>
        <li><router-link to="/contato" @click="closeMenu">Contato</router-link></li>
        </ul>
    </nav>
    </template>

    <script setup>
    import { ref } from 'vue'

    const isOpen = ref(false)

    const toggleMenu = () => {
    isOpen.value = !isOpen.value
    }

    const closeMenu = () => {
    isOpen.value = false
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/variables' as *;
@use '../assets/styles/mixins' as *;

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: $spacing-md $spacing-lg;
    background-color: $color-background-alt;
    position: sticky;
    top: 0;
    z-index: 1000;

    .logo a {
        font-weight: 700;
        font-size: 1.2rem;
        color: $color-primary;
        text-decoration: none;
    }

    .nav-links {
        list-style: none;
        display: flex;
        gap: $spacing-lg;
        transition: all 0.3s ease;

        a {
        color: $color-text;
        font-weight: 500;
        @include transition(color);

        &:hover {
            color: $color-primary;
        }
        }

        /* MOBILE */
        @media (max-width: 768px) {
        position: absolute;
        top: 65px;
        left: 0;
        right: 0;
        background-color: $color-background-alt;
        flex-direction: column;
        align-items: center;
        gap: $spacing-md;
        padding: 1rem 0;
        display: none;
        border-top: 1px solid rgba(255, 255, 255, 0.1);

        &.open {
            display: flex;
            animation: fadeIn 0.3s ease;
        }
        }
    }

    /* Botão hamburguer */
    .menu-toggle {
        display: none;
        background: none;
        border: none;
        cursor: pointer;

        span {
        display: block;
        width: 24px;
        height: 3px;
        background-color: $color-primary;
        position: relative;
        transition: all 0.3s ease;

        &::before,
        &::after {
            content: "";
            position: absolute;
            left: 0;
            width: 24px;
            height: 3px;
            background-color: $color-primary;
            transition: all 0.3s ease;
        }

        &::before {
            top: -8px;
        }

        &::after {
            top: 8px;
        }

        &.open {
            background: transparent;

            &::before {
            transform: rotate(45deg);
            top: 0;
            }

            &::after {
            transform: rotate(-45deg);
            top: 0;
            }
        }
        }

        @media (max-width: 768px) {
        display: block;
        }
    }
    }

    @keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
    }
</style>
