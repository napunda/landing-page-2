<template>
  <v-container class="header pt-8 white--text">
    <header class="d-flex justify-space-between align-center">
      <div class="logo">Marketing Criativo</div>
      <div class="menu d-flex">
        <div class="menu-items ml-lg-5" v-for="item in menu" :key="item.id">
          <v-btn
            class="text-none menu-item"
            color="white"
            text
            :href="item.link"
            >{{ item.name }}</v-btn
          >
        </div>
      </div>
    </header>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    menu: [
      { id: 0, name: "Início", link: "/" },
      { id: 0, name: "Serviços", link: "/#servicos" },
      { id: 0, name: "Sobre", link: "/#sobre" },
      { id: 0, name: "Contato", link: "/#contato" },
      { id: 0, name: "Já tem uma conta?", link: "/#conta" },
    ],
  }),
};
</script>

<style lang="scss" scoped>
.header {
  .logo {
    width: 50px;
    line-height: 30px;
    font-size: 32px;
  }
  .menu-item {
    transition: all 1.15s;
  }
  .menu-items:nth-child(5) {
    border: solid #840ec9 !important;
    border-radius: 10px;
  }
  .menu-item:hover {
    color: #840ec9 !important;
  }
}
</style>
