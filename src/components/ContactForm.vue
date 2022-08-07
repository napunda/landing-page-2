<template>
  <v-container class="white--text pt-lg-16 pt-md-10 pt-5">
    <v-row>
      <v-col cols="12" lg="5" md="6">
        <div class="text-lg-h2 text-md-h2 text-sm-h3 text-h4 font-weight-bold">
          <span class="primary--text">Inscreva-se agora </span> na Newslatter
        </div>
        <div
          class="text-lg-body-1 text-md-body-1 text-body-2 mt-lg-8 mb-lg-8 mt-md-8 mb-md-8 mb-5 mt-5 font-weight-thin"
        >
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptas
          eveniet sapiente cumque ullam quis eaque, iusto impedit illo velit
          repellat exercitationem iste, at sint earum ratione mollitia ipsum
          cupiditate maxime.
        </div>
        <BaseForm />
      </v-col>
      <v-col cols="12" lg="7" md="6">
        <img width="100%" class="d-block" src="/img/img-home.png" alt="Home" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import BaseForm from "../widgets/BaseForm.vue";
export default { components: { BaseForm } };
</script>

<style></style>
