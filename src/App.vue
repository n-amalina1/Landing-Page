<template>
  <v-app>
    <!--
    <v-app-bar app>
      <nav class="navbar navbar-inverse navbar-fixed-top">
        <div class="container-fluid">
          <div class="navbar-header">
            <a class="navbar-brand" href="#">SGUnited</a>
          </div>
          <ul class="nav navbar-nav">
            <li class="active"><a href="#">Home</a></li>
            <li><a href="#">Programs</a></li>
            <li><a href="#">About Us</a></li>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <li>
              <a href="#"
                ><span class="glyphicon glyphicon-user"></span> Sign Up</a
              >
            </li>
            <li>
              <a href="#"
                ><span class="glyphicon glyphicon-log-in"></span> Login</a
              >
            </li>
          </ul>
        </div>
      </nav>
    </v-app-bar>
    -->
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




