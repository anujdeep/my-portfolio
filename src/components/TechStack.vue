<template>
  <div>
    <div id="tech-stack">
      <b-card title="Front End" id="frontend">
        <div
          v-for="tech in frontTech"
          :key="tech.name"
          class="row mb-1"
          style="color: black"
        >
          <div class="col-sm-4 pt-2">{{ tech.name }}:</div>
          <div class="col-sm-8 pt-3">
            <b-progress
              :value="tech.value"
              :key="tech.name"
              height="10px"
              animated
            ></b-progress>
          </div>
        </div>
      </b-card>

      <b-card title="Back End" id="backend">
        <div
          v-for="tech in backTech"
          :key="tech.name"
          class="row mb-1"
          style="color: black"
        >
          <div class="col-sm-4 pt-2">{{ tech.name }}:</div>
          <div class="col-sm-8 pt-3">
            <b-progress
              :value="tech.value"
              :key="tech.name"
              height="10px"
              animated
            ></b-progress>
          </div>
        </div>
      </b-card>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      frontTech: [
        { name: "Vue Js", value: 80 },
        { name: "Angular", value: 60 },
        { name: "Javascript", value: 80 },
        { name: "Vuex", value: 70 },
        { name: "CSS", value: 70 },
      ],
      backTech: [
        { name: "Node Js", value: 50 },
        { name: "Java", value: 70 },
        { name: "SQL", value: 60 },
        { name: "Mongo DB", value: 55 },
        { name: "Python", value: 70 },
      ],
    };
  },
};
</script>
<style scoped>
#tech-stack {
  display: flex;
}
#backend,
#frontend {
  width: 35vw;
  color: gray;
}
#frontend {
  margin-right: 1.6vw;
}

#content {
  display: flex;
}
@media only screen and (max-width: 600px) {
  #tech-stack {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 2vw;
  }
  #backend,
  #frontend {
    width: 100%;
  }
}
</style>
