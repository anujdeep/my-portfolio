<template>
  <div id="profile">
    <div class="left-side">
      <BasicDetails />
      <Experience />
    </div>
    <div class="right-side">
      <TechStack />
      <Project />
      <Qualifications />
    </div>
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
  gap: 3vw;
  height: 55rem;
}
.right-side {
  display: flex;
  flex-direction: column;
  gap: 2vw;
  max-width: 60rem;
}
.left-side {
  max-width: 20rem;
  display: flex;
  flex-direction: column;
  gap: 2vw;
}

@media only screen and (max-width: 600px) {
  #profile {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  .right-side {
    display: flex;
    flex-direction: column;
    gap: 2vw;
    width: 100%;
  }
  .left-side {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 2vw;
  }
}
</style>
