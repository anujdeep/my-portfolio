<template>
  <div>
    <div id="profile">
      <BasicDetails />
      <TechStack />
    </div>
    <div style="display: flex">
      <Experience />
      <Project />
    </div>
    <Qualifications />
  </div>
</template>

<script>
import BasicDetails from "./BasicDetails.vue";
import TechStack from "./TechStack.vue";
import Experience from "./Experience.vue";
import Project from "./Projects.vue";
import Qualifications from "./Qualifications.vue";
export default {
  name: "Profile",
  components: {
    BasicDetails,
    TechStack,
    Experience,
    Project,
    Qualifications,
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#profile {
  display: flex;
  justify-content: space-between;
}
</style>
