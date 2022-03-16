<template>
  <v-app>
    <v-main>
      <Header />
    </v-main>

    <v-footer app> </v-footer>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>




