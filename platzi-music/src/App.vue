<template lang="pug">
  #app
    section.section
      nav.nav.has-shadow
        .container
          input.input.is-large(
            type="text", 
            placeholder="Buscar canciones",
            v-model="searchQuery"
          )
          a.button.is-info.is-large(@click="search") Buscar
          a.button.is-danger.is-large &times;
          p
            small {{ searchMessage }}

      .container.results
        .columns
          .columns(v-for="t in tracks" :key="t.id") {{ t.name }} - {{ t.artist }}
    
</template>

<script>
const tracks = [
  { name: "Muchacha", artist: "Luis Alberto Spinetta" },
  { name: "Baila conmigo", artist: "Davit" },
  { name: "I want to break free", artist: "Quen" }
];

export default {
  name: "app",
  data() {
    return {
      searchQuery: "",
      tracks: []
    };
  },

  computed: {
    searchMessage() {
      return `Encontrados: ${this.tracks.length}`;
    }
  },

  methods: {
    search() {
      this.tracks = tracks;
    }
  }
};
</script>

<style lang="scss">
@import "./scss/main.scss";

.results {
  margin-top: 50px;
}
</style>
