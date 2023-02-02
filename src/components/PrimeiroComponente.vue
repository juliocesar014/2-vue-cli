<template>
  <div>
    <h1>Minha msg : {{ msg }}</h1>
    <MultiplosEventos />
    <ReutilizarComponente />
    <ReutilizarComponente />
    <ReutilizarComponente />
    <ReutilizarComponente />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue";
import ReutilizarComponente from "./ReutilizarComponente.vue";

export default {
  name: "PrimeiroComponente",
  components: {
    MultiplosEventos,
    ReutilizarComponente,
  },

  data() {
    return {
      msg: "Oi 22",
    };
  },
};
</script>
