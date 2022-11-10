<script>
import AppHeader from "./components/AppHeader.vue";
export default {
  components: {
    AppHeader,
  },
};
</script>

<template>
  <img
    class="img"
    src="./assets/breaking-bad-2-180x180-1343174296.png"
    alt="" />
  <AppHeader />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
