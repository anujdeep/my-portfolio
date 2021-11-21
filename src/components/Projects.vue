<template>
  <div>
    <b-card title="Projects" id="project">
      <div
        v-for="project in projects"
        :key="project.name"
        class="row mb-1"
        style="color: black"
      >
        <div class="col-sm-4 pt-2">{{ project.name }}</div>
        <div class="techStack">
          <span v-for="tech in project.techStack" :key="tech">
            #{{ tech }}
          </span>
        </div>
        <div style="font-size: 14px">{{ project.desc }}</div>
        <div>
          <a :href="project.link" target="_blank" id="projectLink"
            >Project Link</a
          >
        </div>
      </div>
    </b-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "Youtube Clone",
          techStack: ["Angular", "Bootstrap"],
          link: "https://xenodochial-bell-da5174.netlify.app/",
          desc: "It is a youtube clone bulit using Angular for desktop.I have used youtube developers api for fetching data from YouTube.Users can see trending videos, search videos,read comments,etc.",
        },
        {
          name: "Team Work Manager",
          techStack: ["Vue Js", "Mongo DB", "Node Js"],
          link: "https://github.com/anujdeep/task_manager",
          desc: "A MEVN based web app used to track progress and completion of projects by an employee of a company.You can use the app to know which employees are free or busy in their projects and what is their average project completion time.",
        },
        {
          name: "Car Rental Webapp",
          techStack: ["HTML", "CSS", "JS", "PHP"],
          link: "https://elated-kalam-26154a.netlify.app/",
          desc: "It is a website built using Wamp server.You can book cab using the demo app.",
        },
      ],
    };
  },
};
</script>
<style scoped>
#project {
  position: absolute;
  width: 61.5vw;
  left: 32.7vw;
  bottom: 10vh;
  color: gray;
}
.techStack {
  flex-direction: column;
  color: grey;
  font-size: 12px;
}
#projectLink {
  text-decoration: none;
  color: black;
  cursor: pointer;
  font-size: 12px;
  color: gray;
}
</style>
