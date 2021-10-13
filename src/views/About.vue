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
          <h1>Loja de Teste</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-img
            width="100%"
            src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
          ></v-img
          ><br />
          <v-chip outlined dark color="#F76F72"><b>Padaria</b></v-chip>
        </v-col>
      </v-row>
      <v-row>
        <v-col> <b>Endereço: </b> Rua do Exemplo, 49 - São Paulo - SP </v-col>
      </v-row>
      <v-row>
        <v-col> <b>Telefone: </b> (11) 91111-2222</v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn color="#25D366" width="150px" dark>WhatsApp</v-btn>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn color="#FF9494" width="150px" dark>Denunciar</v-btn>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "About",
  methods: {
    voltar() {
      this.$router.go(-1);
    },
  },
};
</script>