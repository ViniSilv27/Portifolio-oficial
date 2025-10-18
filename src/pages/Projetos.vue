<template>
    <section class="projetos">
        <h2>Projetos</h2>
        <div class="projects-grid">
        <div
            class="project-card"
            v-for="project in projects"
            :key="project.name"
        >
            <h3>{{ project.name }}</h3>
            <p>{{ project.description }}</p>
            <div class="links">
            <a :href="project.github" target="_blank">GitHub</a>
            <a v-if="project.demo" :href="project.demo" target="_blank">Demo</a>
            </div>
        </div>
        </div>
    </section>
</template>

<script setup>
    const projects = [
    {
    name: "Vingadores – A Era de Ultron",
    description: "Site baseado no filme Vingadores: A Era de Ultron, mostrando personagens e detalhes do enredo.",
    github: "https://github.com/ViniSilv27/vingadores-a-era-de-ultron", 
    demo: "https://vingadores-a-era-de-ultron-68h2-67upop1tb.vercel.app/",
    image: "https://vercel.com/vinicius-projects-856b51f4/vingadores-a-era-de-ultron-68h2/screenshot.png" 
    },
    {
    name: "Comet Instruments",
    description: "Site de apresentação da Comet Instruments, uma loja que inventei com informações sobre produtos e serviços.",
    github: "https://github.com/ViniSilv27/Comet-Instruments", 
    demo: "https://comet-instruments-alh6y09eo-vinicius-projects-856b51f4.vercel.app/",
    image: "https://comet-instruments-alh6y09eo-vinicius-projects-856b51f4.vercel.app/screenshot.png" 
    },
    {
    name: "Optimus Tech",
    description: "Projeto feito como desafio da Alura 7 Days of Coding, mostrando produtos e soluções tecnológicas.",
    github: "https://github.com/ViniSilv27/Optimus-Tech", 
    demo: "https://optimus-tech-blue-pi.vercel.app/",
    image: "https://optimus-tech-blue-pi.vercel.app/screenshot.png"
    },
    {
    name: "Barbearia Urban",
    description: "Projeto feito com Bootstrap para uma barbearia, apresentando serviços e informações de contato.",
    github: "https://github.com/ViniSilv27/barbearia-urban",
    demo: "https://barbearia-urban.vercel.app/",
    image: "https://raw.githubusercontent.com/ViniSilv27/barbearia-urban/main/screenshot.png" 
    },
    {
    name: "Clone Disney+",
    description: "Clone do site da Disney+, desenvolvido em aula, com layout e funcionalidades semelhantes.",
    github: "https://github.com/ViniSilv27/clone_disneyplus",
    demo: "https://clone-disneyplus-eight-kappa.vercel.app/",
    image: "https://raw.githubusercontent.com/ViniSilv27/clone_disneyplus/main/screenshot.png",
    },
    {
    name: "Tabela FIPE",
    description: "Aplicativo em Java que consulta a Tabela FIPE para obter informações de veículos.",
    github: "https://github.com/ViniSilv27/tabela-FIPE",
    demo: "#", 
    image: "https://raw.githubusercontent.com/ViniSilv27/tabela-FIPE/main/screenshot.png" 
    },
    {
    name: "Alurabooks",
    description: "site de vendas de livro feito em aula com a alura",
    github: "https://github.com/ViniSilv27/alurabooks",
    demo: "https://alurabooks-git-main-vinicius-projects-856b51f4.vercel.app/", 
    image: "https://alurabooks-git-main-vinicius-projects-856b51f4.vercel.app/screenshot.png" 
    },
    {
    name: "Jogo do número secreto",
    description: "o objetivo é usar o javascript e suas funcionalidades para montar um jogo interativo",
    github: "https://github.com/ViniSilv27/jogo-do-numero-secreto",
    demo: "https://jogo-do-numero-secreto-6gzf6do5e-vinicius-projects-856b51f4.vercel.app/", 
    image: "https://jogo-do-numero-secreto-6gzf6do5e-vinicius-projects-856b51f4.vercel.app/screenshot.png" 
    },
    {
    name: "Calculadora IMC",
    description: "o objetivo desse projeto simples é utilizr e entender as funcionalidades do vue ",
    github: "https://github.com/ViniSilv27/calculadora-imc",
    demo: "https://calculadora-pdx95xeqr-vinicius-projects-856b51f4.vercel.app/", 
    image: "https://calculadora-pdx95xeqr-vinicius-projects-856b51f4.vercel.app/screenshot.png" 
    },

    ]
</script>

<style lang="scss" scoped>
    @use '../assets/styles/variables' as *;
    @use '../assets/styles/mixins' as *;

    .projetos {
    padding: 4rem 2rem;
    text-align: center;
    color: $color-text;

    h2 {
        color: $color-primary;
        margin-bottom: $spacing-lg;
    }

    p{
        font-size: 1rem;
    }

    .projects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr); // até 3 cards por linha
    gap: $spacing-lg;
    margin-top: $spacing-md;

    @media (max-width: 1024px) {
        grid-template-columns: repeat(2, 1fr); // 2 cards em telas médias
    }

    @media (max-width: 600px) {
        grid-template-columns: 1fr; // 1 card por linha em mobile
    }
}

    .project-card {
        background-color: $color-background-alt;
        padding: $spacing-lg;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        @include transition(transform);

        &:hover {
        transform: translateY(-5px);
        }

        h3 {
        color: $color-primary;
        margin-bottom: $spacing-sm;
        font-size: 1.3rem;
        }

        p {
        color: $color-text-muted;
        margin-bottom: $spacing-md;
        line-height: 1.5;
        }

        .links {
        display: flex;
        justify-content: center;
        gap: $spacing-md;

        a {
            color: $color-primary;
            font-weight: 500;

            &:hover {
            color: $color-secondary;
            }
        }
        }
    }
}
</style>
