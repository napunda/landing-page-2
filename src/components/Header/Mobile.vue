<template>
  <div>
    <v-app-bar class="secondary main-header-mobile elevation-4" app>
      <div class="py-2 d-flex align-end">
        <router-link class="d-flex" to="/">
          <div class="logo white--text text-h5">Marketing Criativo</div>
        </router-link>
      </div>

      <v-spacer />

      <v-app-bar-nav-icon
        color="white"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer class="primary" v-model="drawer" fixed temporary>
      <div class="px-8 py-6 d-flex flex-column">
        <router-link to="/" class="d-flex">
          <div class="logo white--text">Marketing Criativo</div>
        </router-link>
      </div>

      <v-list-item-group v-model="current">
        <v-list>
          <div v-for="({ name, link }, i) in menu" :key="i">
            <v-list-item v-if="link" :to="link" link>
              <v-list-item-content>
                <v-list-item-title
                  class="white--text text-body-2 font-weight-medium nav-link"
                >
                  {{ name }}
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </div>
        </v-list>
      </v-list-item-group>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: this.$route.path,
      drawer: false,
      menu: [
        { id: 0, name: "Início", link: "/" },
        { id: 0, name: "Serviços", link: "/#servicos" },
        { id: 0, name: "Sobre", link: "/#sobre" },
        { id: 0, name: "Contato", link: "/#contato" },
        { id: 0, name: "Já tem uma conta?", link: "/#conta" },
      ],
    };
  },
};
</script>

<style scoped>
a {
  text-decoration: none;
}
.nav-link .icon {
  vertical-align: baseline;
}
</style>

<style>
.main-header-mobile {
  z-index: 610 !important;
}

.main-header-mobile .navbar-brand {
  height: 60px;
}

.v-navigation-drawer__content .navbar-brand {
  height: 100px;
}

.v-navigation-drawer {
  z-index: 620 !important;
}

.v-list-item__icon .v-icon {
  color: #ffffff !important;
  font-size: 14px !important;
}
</style>
