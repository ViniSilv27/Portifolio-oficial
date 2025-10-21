<template>
    <section class="contato">
        <h2>Entre em contato</h2>
        <p>Se você quer conversar sobre estágios, projetos ou tutorias de matemática, me envie uma mensagem!</p>
        
        <div class="buttons">
        <!-- Botão WhatsApp com mensagem pronta -->
        <a
            href="https://wa.me/5519971724794?text=Olá%20Vinicius!%20Gostaria%20de%20entrar%20em%20contato%20sobre%20estágio%20ou%20projetos."
            target="_blank"
            class="btn-primary"
        >
            WhatsApp
        </a>

        <!-- Botão LinkedIn -->
        <a
            href="https://www.linkedin.com/in/vinicius-souza-silva/"
            target="_blank"
            class="btn-secondary"
        >
            LinkedIn
        </a>
        <!-- Botão pra instagram-->
        <a
            href="https://www.instagram.com/vinisilv_18/"
            target="_blank"
            class="btn-secondary"
        >
            Instagram
        </a>
        <!-- Botão pra Github-->
        <a
            href="https://github.com/vinisilv27"
            target="_blank"
            class="btn-secondary"
        >
            GitHub
        </a>

        <!-- Botão para copiar e-mail -->
        <button @click="copyEmail" class="btn-primary">
            Copiar E-mail
        </button>
        </div>
    </section>
    </template>

    <script setup>
    const copyEmail = () => {
    navigator.clipboard.writeText("vinicius.sv27@gmail.com");
    alert("E-mail copiado para a área de transferência!");
    };
    </script>

    <style lang="scss" scoped>
    @use '../assets/styles/variables' as *;
    @use '../assets/styles/mixins' as *;

    .contato {
    padding: 4rem 2rem;
    text-align: center;
    color: $color-text;

    h2 {
        color: $color-primary;
        margin-bottom: $spacing-md;
    }

    p {
        color: $color-text-muted;
        margin-bottom: $spacing-lg;
        line-height: 1.6;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
    }

    .buttons {
        display: flex;
        justify-content: center;
        gap: $spacing-md;
        flex-wrap: wrap;

        a, button {
        padding: $spacing-sm $spacing-md;
        border-radius: 8px;
        font-weight: 500;
        text-decoration: none;
        cursor: pointer;
        transition: background-color 0.3s ease, color 0.3s ease;
        border: none;

        &.btn-primary {
            background-color: $color-primary;
            color: $color-text;
            &:hover {
            background-color: $color-secondary;
            }
        }

        &.btn-secondary {
            border: 2px solid $color-primary;
            color: $color-primary;
            background-color: transparent;
            &:hover {
            background-color: $color-primary;
            color: $color-text;
            }
        }
        }
    }
}
</style>

