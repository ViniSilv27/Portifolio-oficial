<template>
    <section class="home">
        <div class="home-content">
        <!-- Imagem de perfil -->
        <div class="profile-image">
            <img src="../../images/WhatsApp Image 2025-10-15 at 12.09.09 (1).jpeg" alt="Foto de Vinicius Silva" />
        </div>

        <h1>Olá, eu sou Vinicius Silva</h1>

        <p>
            Estudante de Ciência de Dados e desenvolvedor front-end em formação.
            Estou sempre aprendendo novas tecnologias, criando projetos práticos
            e buscando desafios que me façam evoluir rapidamente.
        </p>

        <p>
            Meu foco atual é ingressar na área de Ciência de Dados, aplicando análise de dados, estatística e aprendizado de máquina em projetos reais. 
            Além disso, possuo conhecimentos em desenvolvimento front-end com Vue 3, Sass e JavaScript, que uso para criar dashboards e visualizações interativas.
            Explore meus projetos abaixo e sinta-se à vontade para entrar em contato!
        </p>

        <div class="buttons">
            <router-link to="/projetos" class="btn-primary">Ver Projetos</router-link>
            <router-link to="/contato" class="btn-secondary">Entrar em Contato</router-link>
        </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../assets/styles/variables' as *;
    @use '../assets/styles/mixins' as *;

    .home {
    min-height: 80vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: $spacing-lg;

    .home-content {
        max-width: 800px;
        text-align: center;
        color: $color-text;

        /* Imagem de perfil */
        .profile-image {
        display: flex;
        justify-content: center;
        margin-bottom: $spacing-md;

        img {
            width: 160px;
            height: 160px;
            object-fit: cover;
            border-radius: 50%;
            border: 4px solid $color-primary;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;

            &:hover {
            transform: scale(1.05);
            }

            @media (max-width: 600px) {
            width: 120px;
            height: 120px;
            }
        }
        }

        h1 {
        font-size: 2.5rem;
        color: $color-primary;
        margin-bottom: $spacing-md;

        @media (max-width: 600px) {
            font-size: 2rem;
        }
        }

        p {
        color: $color-text-muted;
        line-height: 1.6;
        margin-bottom: $spacing-md;
        }

        .buttons {
        display: flex;
        justify-content: center;
        gap: $spacing-md;
        flex-wrap: wrap;

        .btn-primary,
        .btn-secondary {
            padding: $spacing-sm $spacing-md;
            border-radius: 8px;
            font-weight: 500;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }

        .btn-primary {
            background-color: $color-primary;
            color: $color-text;
            &:hover {
            background-color: $color-secondary;
            }
        }

        .btn-secondary {
            border: 2px solid $color-primary;
            color: $color-primary;
            &:hover {
            background-color: $color-primary;
            color: $color-text;
            }
        }
        }
    }
    }
</style>



