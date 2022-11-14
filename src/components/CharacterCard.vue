<script>
// import CharactersApp from "./CharactersApp.vue";
export default {
  name: "CharacterCard",
  props: {
    character: Object,
  },
};
</script>

<template>
  <div class="character-item text-center">
    <img class="rounded-circle" :src="character.img" alt="" />
    <h4>{{ character.name }}</h4>
  </div>
</template>

<style lang="scss" scoped></style>
