<template>
  <div id="app">
    <Profile />
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";

export default {
  name: "App",
  components: {
    Profile,
  },
};
</script>

<style>
#app {
  margin: 60px;
}
</style>
