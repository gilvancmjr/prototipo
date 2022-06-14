<template>
  <v-card>
    <v-card-text>
      <v-container>
        <v-row>
          <v-col cols="12" sm="6" md="5">
            <v-toolbar-title><h1>Cadastrar Usuario</h1></v-toolbar-title>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6" md="4">
            <h3>Nome</h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="12" md="12">
            <v-text-field
              outlined
              dense
              placeholder="Informe seu nome"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6" md="4">
            <h3>E-mail</h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="12" md="12">
            <v-text-field
              outlined
              dense
              placeholder="Informe seu e-mail"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6" md="4">
            <h3>Senha</h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="12" md="12">
            <v-text-field
              v-model="password"
              :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show2 ? 'text' : 'password'"
              name="input-10-1"
              counter
              outlined
              dense
              @click:append="show2 = !show2"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6" md="4">
            <h3>Confirme sua senha</h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="12" md="12">
            <v-text-field
              v-model="password"
              :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show1 ? 'text' : 'password'"
              name="input-10-1"
              counter
              outlined
              dense
              @click:append="show1 = !show1"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="6" md="6">
            <h3>Permissão</h3>
          </v-col>
          <v-col cols="12" sm="6" md="6">
            <h3>Status</h3>
          </v-col>
        </v-row>

        <v-row>
          <v-col cols="12" sm="6" md="6">
            <v-autocomplete
              outlined
              dense
              placeholder="Selecione..."
            ></v-autocomplete>
          </v-col>
          <v-col cols="12" sm="6" md="6">
            <v-autocomplete
              outlined
              dense
              placeholder="Selecione..."
            ></v-autocomplete>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" sm="3" md="2">
            <v-btn
              to="/user/consulta-user"
              color="primary"
              dark
              class="mb-2"
              left
            >
              <v-icon dark left>mdi-arrow-left </v-icon>

              Voltar
            </v-btn>
          </v-col>
          <v-col cols="2" sm="1" md="1">
            <v-btn
              color="primary"
              dark
              class="mb-2"
              left
            >
              <v-icon dark left>mdi-account-check</v-icon>

              Salvar
            </v-btn>
          </v-col>
        </v-row>
        
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script >
export default {
  data() {
    return {
      show1: false,
      show2: false,
      password: "Password",
      rules: {
        required: (value) => !!value || "Required.",
      },
    };
  },
};
</script>

<style>
</style>