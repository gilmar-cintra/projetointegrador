<template>
  <v-col cols="6" @click="vaParaSobre()">
    <v-img
      width="100%"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>
    <v-card elevation="2">
      <v-card-title>Loja de Teste</v-card-title>
      <v-card-text>
        <v-chip outlined dark color="#F76F72"><b>Padaria</b></v-chip
        ><br /><br />2 KM</v-card-text
      >
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "LojaCard",
  methods: {
    vaParaSobre() {
      this.$router.push("/about");
    },
  },
};
</script>

<style lang="scss" scoped>
</style>