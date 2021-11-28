<template>
  <div>
    <b-card img-top tag="article">
      <b-card-img :src="require('../assets/myPic.jpeg')"></b-card-img>
      <b-card-text>
        <div id="name">Anuj Deep</div>
        <div id="role">FullStack developer</div>
        <div>
          <img src="../assets/email.png" id="img" /><span>
            anujdeepktr@gmail.com</span
          >
        </div>
        <div>
          <img id="linkedin-pic" src="../assets/linkedin.svg" /><span
            ><a
              href="https://in.linkedin.com/in/anuj-deep-342312161"
              target="_blank"
              >My Linkedin</a
            ></span
          >
        </div>
        <div>
          <img id="github-pic" src="../assets/github.svg" /><span
            ><a href="https://github.com/anujdeep" target="_blank">My Github</a>
          </span>
        </div>
        <div style="margin-top: 10px">
          I am a full stack developer, having experience of working in Vue Js,
          Angular, Java and Node Js.
        </div>
      </b-card-text>
    </b-card>
  </div>
</template>
<style scoped>
div {
  color: gray;
}
#name {
  font-weight: 500;
  font-size: 26px;
  padding-top: 5px;
  color: black;
}
#role {
  font-size: 14px;
  color: gray;
}
#img {
  height: 25px;
  width: 25px;
}
img + span {
  padding-left: 10px;
}
a {
  text-decoration: none;
  color: gray;
  cursor: pointer;
}
#linkedin-pic {
  height: 24px;
  width: 30px;
  margin-left: -2px;
  margin-right: 2px;
}
#github-pic {
  margin-left: 2px;
  margin-right: 4px;
}
</style>
