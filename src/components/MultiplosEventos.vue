<template>
  <div>
    <button @click="primeiro(), segundo(), teceiro()">
      Ativar Multiplos Eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiplosEventos",
  data() {
    return {
      multiplos_eventos: "",
    };
  },
  methods: {
    primeiro() {
      this.multiplos_eventos = "Primeiro Evento Ativado";
    },
    segundo() {
      setTimeout(
        () => (this.multiplos_eventos = "Segundo Evento Ativado"),
        2000
      );
    },
    teceiro() {
      setTimeout(() => (this.multiplos_eventos = ""), 3000);
    },
  },
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>
