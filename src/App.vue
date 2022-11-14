<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import CharactersApp from "./components/CharactersApp.vue";
// import CharacterCard from "./components/CharacterCard.vue";
import { store } from "./store";

export default {
  components: {
    AppHeader,
    CharactersApp,
    // CharacterCard,
  },
  data() {
    return {
      store,
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data.results;
    });
  },
};
</script>

<template>
  <img
    class="img"
    src="./assets/breaking-bad-2-180x180-1343174296.png"
    alt="" />
  <AppHeader />
  <main>
    <CharactersApp />
  </main>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
