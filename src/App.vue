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
@media only screen and (max-width: 600px) {
  #app {
    margin: 30px 10px;
  }
}
</style>
