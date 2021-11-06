<template>
  <v-col cols="6" @click="vaParaSobre(id++)">
    <v-img width="100%" :src="loja.imagem"></v-img>
    <v-card elevation="2">
      <br />
      <h4>{{ loja.nome }}</h4>
      <v-card-text>
        <v-chip outlined dark color="#F76F72"
          ><b>{{ loja.categoria }}</b></v-chip
        ><br /><br />{{ loja.distancia }} KM</v-card-text
      >
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "LojaCard",
  props: {
    loja: {
      type: Object,
    },
    id: {
      type: Number,
    },
  },

  methods: {
    vaParaSobre() {
      this.$router.push(`/about/${this.id}`);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>