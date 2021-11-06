<template>
  <div class="about">
    <v-toolbar elevation="1" dark color="#F76F72">
      <v-icon @click="voltar()" color="white" left
        >mdi-arrow-left-circle</v-icon
      >

      DETALHES DO COMERCIANTE
    </v-toolbar>
    <v-footer color="#F76F72" app></v-footer>
    <v-container>
      <v-row>
        <v-col>
          <h1>{{ loja.nome }}</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-img width="100%" :src="loja.imagem"></v-img><br />
          <v-chip outlined dark color="#F76F72"
            ><b>{{ loja.categoria }}</b></v-chip
          >
        </v-col>
      </v-row>
      <v-row>
        <v-col> <b>Endereço: </b> {{ loja.endereco }} </v-col>
      </v-row>
      <v-row>
        <v-col> <b>Telefone: </b> {{ loja.telefone }}</v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn
            color="#25D366"
            width="150px"
            :href="`https://wa.me/${loja.telefone}`"
            dark
            >WhatsApp</v-btn
          >
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn color="#FF9494" width="150px" dark>Denunciar</v-btn>
        </v-col>
      </v-row>
    </v-container>
    <br />
  </div>
</template>

<script>
import { lojas } from "../utils/dados.ts";

export default {
  name: "About",
  data() {
    return {
      lojasCadastradas: [],
    };
  },

  methods: {
    voltar() {
      this.$router.go(-1);
    },
  },

  computed: {
    loja() {
      return lojas.find((x) => x.id == this.$route.params.id);
    },
  },
};
</script>