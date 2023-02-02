<template>
  <div>
    <p>{{ email }}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Não estou trabalhando</p>
    <p>Utilizo as seguintes tecnologias p/ back-end:</p>
    <ul>
      <li v-for="(techback, index) in backend_tech" v-bind:key="index">
        {{ techback }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias p/ front-end:</p>
    <ul>
      <li v-for="techfront in frontend_tech" v-bind:key="techfront.id">
        {{ techfront.name }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ botao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">
      Para acessar meu portfolio
      <a v-bind:href="meu_link" target="_blank">Clique aqui</a>
    </p>
    <PictureComponente />
  </div>
</template>

<script>
import PictureComponente from "./PictureComponente.vue";

export default {
  name: "InfoComponente",
  components: {
    PictureComponente,
  },
  props: {
    email2: String,
    email: String,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      meu_link: "https://google.com",
      botao: "Mostrar email",
      backend_tech: ["Python", "Flask", "MySQL", "Docker"],
      frontend_tech: [
        { id: 1, name: "Vue" },
        { id: 2, name: "HTML" },
        { id: 3, name: "CSS" },
      ],
    };
  },

  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.botao = "Mostrar email";
      } else {
        this.botao = "Esconder email";
      }
    },
  },
};
</script>

<style>
.teste2 {
  color: blue;
}
</style>
