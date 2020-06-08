<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <v-row>
          <v-col class="d-inline-flex">
          <p class="display-4 font-weight-black red--text text--darken-4 mr-4">Oscar Baracos</p>
          <v-btn fab icon x-large color="red darken-4" href="https://github.com/Oscbacon">
            <v-icon x-large>fab fa-github</v-icon>
          </v-btn>
          <v-btn fab icon x-large color="red darken-4" href="https://www.linkedin.com/in/oscar-baracos-102ba4145/">
            <v-icon x-large>fab fa-linkedin-in</v-icon>
          </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
};
</script>
