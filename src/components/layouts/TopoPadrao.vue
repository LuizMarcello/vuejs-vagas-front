<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container">
      <a class="navbar-brand" href="#">Vagas</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <!-- Diretiva v-on(@)evento de click, quando clicar em "home" -->
            <!--  <a class="nav-link" href="#" @click="navegarPara()">Home</a> -->
            <a class="nav-link" href="#" @click="navegarPara('Home')">Home</a>
          </li>
          <li class="nav-item">
            <!-- Diretiva v-on(@)evento de click, quando clicar em "Publicar vaga" -->
            <!-- <a class="nav-link" href="#" @click="navegarPara()">Publicar vaga</a -->
            <a class="nav-link" href="#" @click="navegarPara('PublicarVaga')"
              >Publicar vaga</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
/* Para codificar e exportar o objeto de configuração do vueJS, para o componente */
export default {
  name: "TopoPadrao",
  methods: {
    navegarPara(p) {
      /* $emit(): Método que permite emitir um evento para o componente pai */
      /* Como 1º parâmetro: nome do evento que será capturado no componenete pai */
      /* Como 2º parâmetro(Opcional): payload, string, objeto, array, função de call-back */
      this.$emit("navegar", p);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
/* Define o estilo específico, somente para este componente */
</style>
