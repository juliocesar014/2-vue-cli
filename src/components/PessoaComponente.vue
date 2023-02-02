<template>
  <div>
    <h2>Essa é a descrição da pessoa: {{ nome }}</h2>
    <InfoComponente v-bind:email="email" />
    <FormComponente />
  </div>
</template>

<script>
import InfoComponente from "./InfoComponente.vue";
import FormComponente from "./FormComponente.vue";

export default {
  components: {
    InfoComponente,
    FormComponente,
  },
  name: "PessoaComponente",
  data() {
    return {
      nome: "Júlio",
      email: "jojo@gmail.com",
    };
  },
};
</script>
