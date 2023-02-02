<template>
  <div>
    <button @click="$emit('mudarImagem')">Trocar imagem do Perfil</button>
  </div>
</template>

<script>
export default {
  name: "MudarImagem",
  emits: ["mudarImagem"],
};
</script>
