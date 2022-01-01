<template>
 
  <div class="background"></div>
  <div class="info d-flex justify-content-between">
    <div style="display: flex">
      <div class="bg-image"></div>
      <div style="position: relative; margin-top: 60px">
        <div>{{ name }}</div>
        <div style="font-size: 15px; font-weight: 100">{{ description }}</div>
      </div>
    </div>
    <div
      style="position: relative;  margin-top: 70px; top: 70px display: flex; padding-right: 10px;"
    >
     <a download="logo" href="logo.png"  target="_blank">
      <MDBBtn outline="primary" style="margin-right: 10px; margin-bottom: 4px" 
        >
       View Resume
        </MDBBtn
      >
      </a>

      <a href="mailto:name@email.com">
        <MDBBtn color="primary" style="margin-bottom: 4px"
        ><MDBIcon icon="paper-plane" iconStyle="far" style="padding-right: 8px"  />
        Email</MDBBtn
      >
      </a>
      
    </div>
  </div>

  <div style="margin-top: 140px; padding-left: 25px; padding-right: 25px">
    <hr />
  </div>
    <AboutComp />
  
  <div style="margin-top: 10px; padding-left: 25px; padding-right: 25px">
    <hr />
  </div>
  <ExperienceComp />
  
  <div style="margin-top: 10px; padding-left: 25px; padding-right: 25px">
    <hr />
  </div>
  <ProjectComp />
  
  <div style="margin-top: 10px; padding-left: 25px; padding-right: 25px">
    <hr />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutComp from '@/components/AboutComp.vue';
import ExperienceComp from '@/components/Experience/ExperienceComp.vue';
import ProjectComp from '@/components/Projects/ProjectComp.vue'
import { MDBBtn, MDBIcon, } from "mdb-vue-ui-kit";


export default {
  name: "Home",
  components: {
   
    AboutComp,
    MDBBtn,
    MDBIcon,
    ExperienceComp, 
    ProjectComp,
  },
  data() {
    return {
      name: "Michael Opoku",
      description: "I'm a web and mobile developer based in Accra, Ghana",
    };
  },
};
</script>

<style scoped>
.background {
  background: linear-gradient(45deg, #80ffdb, #5390d9);
  height: 150px;
}

.info {
  display: flex;
  background: transparent;
  position: absolute;
  top: 120px;
  width: 100%;
}

.bg-image {
  background-image: url("../../public/img/user.png");
  background-size: fill;
  height: 120px;
  width: 120px;
  border-radius: 50%;
  border: 3px solid white;

  margin: 10px;
  box-shadow: none;
  -webkit-box-shadow: 0 0 5px rgb(151, 151, 151);
  -moz-box-shadow: 0 0 5px rgb(151, 151, 151);
}
</style>