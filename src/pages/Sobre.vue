<template>
    <section class="sobre">
        <h2>Sobre mim</h2>
        <div class="sobre-content">
        <p>
            Meu nome é Vinicius Silva e atualmente sou estudante de Ciência de Dados na UNIVESP. Anteriormente, já ingressei na Unicamp e na UNIFAL de Poços de Caldas, e hoje sigo minha formação em formato EAD pela UNIVESP.
        </p>
        <p>
            Embora esteja no início da minha formação em Ciência de Dados, já possuo conhecimentos adquiridos em outros cursos complementares. Além disso, estou realizando o curso de Full Stack Java pela EBC, onde desenvolvi habilidades em front-end, incluindo Vue 3, Sass e JavaScript.
        </p>
        <p>
            Sou uma pessoa <strong>curiosa, dedicada e com grande capacidade de aprendizado rápido</strong>, características que aplico tanto nos meus estudos quanto em projetos práticos. Atualmente, busco <strong>estágio na área de Ciência de Dados e Análise de Dados</strong>, visando aplicar meus conhecimentos em desafios reais.
        </p>
        <p>
            Paralelamente, também atuo como tutor na área de Matemática, auxiliando estudantes do ensino fundamental, médio, vestibulares e concursos públicos, o que reforça minha habilidade de comunicação e didática.
        </p>
        </div>
    </section>
    </template>

    <style lang="scss" scoped>
    @use '../assets/styles/variables' as *;
    @use '../assets/styles/mixins' as *;

    .sobre {
    padding: 4rem 2rem;
    color: $color-text;
    text-align: center;

    h2 {
        color: $color-primary;
        margin-bottom: $spacing-lg;
    }

    .sobre-content {
        max-width: 800px;
        margin: 0 auto;
        text-align: left;
        line-height: 1.7;

        p {
        margin-bottom: $spacing-md;
        color: $color-text-muted;

        strong {
            color: $color-text;
        }
        }
    }

    @media (max-width: 768px) {
        .sobre-content {
        padding: 0 $spacing-md;
        font-size: 1rem;
        }
    }
}
</style>
