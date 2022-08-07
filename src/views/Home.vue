<template>
  <v-sheet class="home secondary">
    <Desktop v-if="!smAndDown" />
    <Mobile v-else />
    <ContactForm />
  </v-sheet>
</template>

<script>
import Desktop from "../components/Desktop.vue";
import ContactForm from "../components/ContactForm.vue";
import Mobile from "../components/Header/Mobile.vue";
export default {
  computed: {
    smAndDown() {
      return this.$vuetify.breakpoint.smAndDown;
    },
  },
  name: "Home",
  components: {
    ContactForm,
    Mobile,
    Desktop,
  },
};
</script>
<style lang="scss">
.home {
  font-family: "Poppins", sans-serif;
  height: 100% !important;
}
</style>
