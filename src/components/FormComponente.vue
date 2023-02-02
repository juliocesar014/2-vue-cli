<template>
  <div>
    <form action="" @submit="enviarForm($event)">
      <div><input type="text" v-model="name" /></div>
      <div><input type="email" v-model="email" /></div>
      <SubmitComponente />
      <p>Contéudo</p>
      <p>Contéudo</p>
      <p>Contéudo</p>
    </form>
  </div>
</template>

<script>
import SubmitComponente from "./Form/SubmitComponente.vue";

export default {
  name: "FormComponente",
  components: {
    SubmitComponente,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    enviarForm(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("Form enviado");
      console.log(`O nome é: ${name}`);
      console.log(`O email é: ${email}`);

      // AJAX
      // Inserir os dados no banco de dados
    },
  },
};
</script>

<style scoped>
p {
  margin: 150px;
}
</style>
