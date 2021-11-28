<template>
  <div>
    <b-card title="Qualifications" id="qualification">
      <div
        v-for="qualification in qualifications"
        :key="qualification.name"
        class="row mb-1"
        style="color: black"
      >
        <div class="pt-2">{{ qualification.name }}</div>
        <div
          style="
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            color: gray;
          "
        >
          <div class="pt-2">{{ qualification.Course }}</div>
          <div class="pt-2">{{ qualification.Percentage }}%</div>
        </div>
      </div>
    </b-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      qualifications: [
        {
          name: "Techno India College of Technology, Kolkata",
          Course: "B.Tech(Computer Science Eng.)",
          Percentage: 74.8,
        },
        {
          name: "Jawahar Navodaya Vidyalaya, Katihar",
          Course: "Science(PCM)",
          Percentage: 87.6,
        },
      ],
    };
  },
};
</script>
<style scoped>
#qualification {
  /* position: absolute;
  left: 32.7vw;
  bottom: -16vh; */
  /* width: 71.6vw; */
  color: gray;
  margin-bottom: 3vh;
}
</style>
