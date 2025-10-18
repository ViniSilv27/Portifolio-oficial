<template>
  <div id="app"> <Navbar />
    
    <main class="main-content">
      <router-view /> 
    </main>
    
    <Footer />
  </div>
</template>

<script setup>
  import Navbar from './components/Navbar.vue'
  import Footer from './components/Footer.vue'
</script>

<style>
/* Reset básico, se ainda não tiver feito */
html, body {
  margin: 0;
  padding: 0;
}

#app {
  /* 1. Define o contêiner para usar Flexbox na vertical */
  display: flex;
  flex-direction: column;
  
  /* 2. Garante que o contêiner ocupe no mínimo 100% da altura da viewport (tela visível) */
  min-height: 100vh;
}

.main-content {
  /* 3. Faz com que o conteúdo principal (onde as páginas carregam) 
        cresça e preencha todo o espaço restante disponível, 
        "empurrando" o rodapé para baixo. */
  flex-grow: 1;
}

/* Os estilos do seu Navbar e Footer permanecem normais, sem `position: fixed` ou `absolute` */
</style>