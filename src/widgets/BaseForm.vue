<template>
  <v-form v-model="valid">
    <v-text-field
      v-model="firstname"
      :rules="nameRules"
      label="Nome"
      required
      solo
      rounded
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
      solo
      rounded
    ></v-text-field>

    <v-btn
      rounded
      color="white"
      class="text-none primary font-weight-regular px-16 py-6"
      type="submit"
    >
      Enviar
    </v-btn>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    firstname: "",
    nameRules: [(v) => !!v || "Digite seu nome"],
    email: "",
    emailRules: [
      (v) => !!v || "Digite seu endereço de e-mail",
      (v) => /.+@.+/.test(v) || "O e-mail deve ser válido",
    ],
  }),
};
</script>
<style></style>
