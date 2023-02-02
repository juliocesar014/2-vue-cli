<template>
  <div>
    <HeaderComponente :esta_logado="true" />
    <PrimeiroComponente />
    <p class="teste2">Meu nome é: {{ nome }}</p>
    <LifeCycle />
    <PessoaComponente />
  </div>
</template>

<script>
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycle from "./components/LifeCycle.vue";
import PessoaComponente from "./components/PessoaComponente.vue";
import HeaderComponente from "./components/HeaderComponente.vue";

export default {
  name: "App",
  components: {
    PrimeiroComponente,
    LifeCycle,
    PessoaComponente,
    HeaderComponente,
  },
  data() {
    return {
      nome: "Nome aqui",
    };
  },
};
</script>

<style>
body {
  background-color: grey;
  color: white;
}

a {
  color: red;
}

.teste {
  color: blue;
}
</style>
