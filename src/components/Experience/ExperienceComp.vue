<template>
  <MDBRow style="padding-left: 25px; padding-right: 25px">
    <MDBCol col="3">Experience</MDBCol>
    <MDBCol col="1"> </MDBCol>
    <MDBCol md="4" v-for="experience in experiences" :key="experience.company">
      <ExperienceCard
        :position="experience.position"
        :company="experience.company"
        :timeLine="experience.timeLine"
        :image="experience.image"
        v-on:openModal="openModal(experience.company)"
      >
        <MDBIcon
          v-for="icon in experience.icons"
          :key="icon"
          :icon="icon"
          iconStyle="fab"
          style="display: inline-block; margin-right: 15px"
        />
      </ExperienceCard>
    </MDBCol>
  </MDBRow>

  <MDBModal
    id="exampleModal"
    tabindex="-1"
    labelledby="exampleModalLabel"
    v-model="exampleModal"
    fullscreen
  >
    <MDBModalHeader>
      <MDBModalTitle id="exampleModalLabel"> {{this.type === this.UvitechGH ? 'Uvitech GH' : 'Freelance'}} </MDBModalTitle>
    </MDBModalHeader>
    <MDBModalBody>
      <MDBRow>
        <MDBCol  md="3" v-for="project in type" :key="project.projectName">
          <ProjectCard
            :projectName="project.projectName"
            :description="project.description"
            :image="project.image"
            v-on:viewProject="viewProject(project.link)"
          >
            <MDBIcon
              v-for="icon in project.icons"
              :key="icon"
              :icon="icon"
              iconStyle="fab"
              style="display: inline-block; margin-right: 15px;"
            />
          </ProjectCard>
        </MDBCol>
      </MDBRow>
    </MDBModalBody>
  </MDBModal>
</template>

<script>
import {
  MDBCol,
  MDBRow,
  MDBIcon,
  MDBModal,
  MDBModalHeader,
  MDBModalTitle,
  MDBModalBody,
} from "mdb-vue-ui-kit";
import ExperienceCard from "../Experience/ExperienceCard.vue";
import ProjectCard from "../Experience/ProjectCard.vue";
import { ref } from "vue";
export default {
  components: {
    MDBCol,
    MDBRow,
    ExperienceCard,
    MDBModal,
    MDBIcon,
    MDBModalHeader,
    MDBModalTitle,
    MDBModalBody,
    ProjectCard,
  },
  data() {
    return {
      type: null,

      experiences: [
        {
          position: "Mobile & Web Development",
          company: "UvitechGH",
          timeLine: " August 2020 - Present",
          image: "uvitech.jpeg",
          icons: ["google-play", "chrome"],
        },
        {
          position: "Mobile & Web Development",
          company: "Freelance",
          timeLine: " November 2018 - Present",
          image: "freelance.jpeg",
          icons: ["app-store-ios", "google-play", "chrome", "github"],
        },
      ],
      UvitechGH: [
        {
          projectName: "UelloSend",
          description:
            "UelloSend is a BULK SMS solution platform powered by UviTech, Inc.",
          image: "uellosend.png",
          icons: ["google-play", "chrome"],
          link: ""
        },
        {
          projectName: "ExPal",
          description:
            "EXPal is a  platform that enables you to exchange virtual currencies.",
          image: "expal.png",
          icons: ["google-play", "chrome"],
          link: "https://expal.uvitechgh.com"
        },
      ],
      FreeLance: [
        {
          projectName: "Cornerstone Giving",
          description:
            "Cornerstone is a free giving and engagement app for all organizations.",
          image: "cornerstone.png",
          icons: ["google-play", "app-store-ios"],
        },
         {
          projectName: "Smart Home",
          description:
            "A flutter cloned ui design of a smart home application.",
          image: "smarthome.png",
          icons: ["github",],
        },
         {
          projectName: "Yellow Taxi",
          description:
            "A flutter cloned ui design of a taxi booking application.",
          image: "taxiApp.png",
          icons: ["github",],
        },
      ],
    };
  },
  methods: {
    openModal(name) {
      console.log("open modal");
      this.type = name === 'UvitechGH' ? this.UvitechGH : this.FreeLance;
      this.exampleModal = true;
      console.log(name);
    },
      viewProject(name) {
   
      console.log(name);
    },
  },
  setup() {
    const exampleModal = ref(false);

    return {
      exampleModal,
    };
  },
};
</script>
