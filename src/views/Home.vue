<template>
  <div class="home">
    <v-toolbar elevation="1" dark color="#F76F72">
      <!-- <v-icon v-if="voltar" color="primary" left
          >mdi-arrow-left-circle</v-icon
        > -->

      SELECIONE O COMERCIO OU SERVIÇO DESEJADO
    </v-toolbar>
    <v-footer color="#F76F72" app></v-footer>
    <br />
    <v-container>
      <v-row>
        <v-col>
          <img src="../assets/logo.png" height="150px" /><br /><br />
        </v-col>
      </v-row>
      <v-card>
        <v-row>
          <v-col cols="10">
            <v-text-field
              class="ml-4"
              dense
              label="Buscar ..."
              hide-details
            ></v-text-field>
          </v-col>
          <v-col cols="2">
            <v-icon color="primary" large>mdi-filter-variant</v-icon>
          </v-col>
        </v-row>
      </v-card>
      <br /><br />
      <v-row>
        <LojaCard v-for="n in 10" :key="n" />
      </v-row>
      <br />
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import LojaCard from "../components/LojaCard.vue";
export default {
  name: "Home",
  components: {
    LojaCard,
  },
};
</script>
