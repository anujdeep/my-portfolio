<template>
  <div>
    <b-card title="Experience" id="experience">
      <div
        v-for="experience in experiences"
        :key="experience.company"
        class="mb-2 experience-content"
      >
        <div v-if="experience.company == 'Card91'">
          <img id="company-1" src="../assets/card91.png" alt="card91" />
        </div>
        <div v-else>
          <img id="company-2" src="../assets/gep.jpeg" alt="gep" />
        </div>
        <div
          id="experience-info"
          :class="{ contentMargin: experience.company == 'GEP' }"
        >
          <div style="display: flex">
            <div>{{ experience.date.from }}</div>
            <div>-</div>
            <div>{{ experience.date.to }}</div>
          </div>
          <div style="color: black; font-size: 14px">{{ experience.role }}</div>
          <div style="padding-top: 10px">{{ experience.desc }}</div>
        </div>
      </div>
    </b-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      experiences: [
        {
          image: "../assets/card91.png",
          company: "Card91",
          date: {
            from: "Sep 2021",
            to: "Current",
          },
          role: "FrontEnd Developer",
          desc: "Designing Portal for credit card and its management",
        },
        {
          image: "../assets/gep.jpeg",
          company: "GEP",
          date: {
            from: "Feb 2021",
            to: "Aug 2021",
          },
          role: "Full Stack Developer",
          desc: "Created the  web app for Automation bot trigger using Angular and Java",
        },
      ],
    };
  },
};
</script>
<style scoped>
#experience {
  width: 57.3%;
  height: 41.5vh;
}
#company-1 {
  width: 5vw;
  height: 10vh;
}
#company-2 {
  width: 5vw;
  height: 10vh;
}
.experience-content {
  display: flex;
  justify-content: space-between;
}
#experience-info {
  padding-top: 2vh;
  margin-left: 2.2vw !important;
}
.contentMargin {
  padding-right: 1.5vw;
  margin-left: 2.2vw !important;
}
div {
  color: gray;
  font-size: 12px;
}
</style>
