<template>
  <div id="app">
    <img src="./assets/logo.png">
    <v-layout row wrap>
      <v-flex xs10 offset-xs1>
        <vuetify-google-autocomplete
          id="id"
          v-on:placechanged="getAddressData"
          v-on:no-results-found="noResultsFound"
          >
        </vuetify-google-autocomplete>
      </v-flex>
    </v-layout>

    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    getAddressData() {
      // Do something...
    },
    noResultsFound() {
      // Do something...
    },
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
