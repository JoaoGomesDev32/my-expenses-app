<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
});
</script>

<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Controle de Despesas Mensais</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

    <v-footer app color="primary" dark>
      <span class="mx-auto">&copy; 2025 - Desenvolvido por João Gomes</span>
    </v-footer>
  </v-app>
  <!-- <div>
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
@import '@/assets/styles/_variables.scss';

body {
  font-family: Arial, sans-serif;
  background-color: #333;
  margin: 0;
  padding: 0;
}

.v-app-bar, .v-footer {
  font-weight: bold;
}
</style>
