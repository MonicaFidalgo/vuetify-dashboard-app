<template>
  <v-app>
    <v-app-bar
      app
      class="navbar"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Dash.io Name"
          class="shrink mr-2 hidden-md-and-up"
          contain
          src="./assets/Dash.io.svg"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Dash.io Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="./assets/Dash.io.svg"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <SideBar />
    </v-main>
  
  </v-app>
</template>

<script>
import SideBar from './components/SideBar';


export default {
  name: 'App',
  components: {
    SideBar
  }
};
</script>
