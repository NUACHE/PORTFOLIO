<template>
  <MDBRow style="padding-left: 25px; padding-right: 25px">
    <MDBCol col="3">About Me</MDBCol>
    <MDBCol col="9">
      <MDBRow>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. molestiae in
        labore corrupti eius?
      </MDBRow>
      <MDBRow>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt omnis
        atque maiores eius voluptate officiis!
      </MDBRow>
      <MDBRow>
        <a
          href="#"
          class="text-decoration-none"
          style="padding-right: 0px; padding-left: 0px; color: #7055a0"
          >Read more</a
        >
      </MDBRow>

      <MDBRow
        style="
          border-radius: 10px;
          background-color: #f9f5fe;
          padding-left: 0px;
          padding-right: 0px;
        "
      >
        <MDBCol col="4" style="padding: 15px">
          <p>Front-end</p>

          <a href="https://flutter.dev" target="_blank">
            <img
              src="../assets/svgs/flutter.svg"
              alt="Flutter SVG"
              style="
                width: 30px;
                height: 30px;
                margin-right: 10px;
                margin-bottom: 10px;
              "
            />
          </a>
          <a href="https://vuejs.org" target="_blank">
            <img
              src="../assets/svgs/vue.svg"
              alt="Vue SVG"
              style="
                width: 30px;
                height: 30px;
                margin-right: 10px;
                margin-top: 0px; ;
              "
            />
          </a>
          <a href="https://mdbootstrap.com" target="_blank">
            <img
              src="../../public/img/mdb.png"
              alt="MDB SVG"
              style="
                width: 60px;
                height: 20px;
                margin-right: 10px;
                margin-top: 0px;
                margin-bottom: 10px;
              "
            />
          </a>
          <a href="https://jquery.com" target="_blank">
            <img
              src="../assets/svgs/jquery.svg"
              alt="jQuery SVG"
              style="width: 30px; height: 50px; margin-bottom: 10px"
            />
          </a>
        </MDBCol>
        <MDBCol col="4" style="padding: 15px">
          <p>Design</p>

          <a href="https://www.figma.com" target="_blank">
            <img
              src="../assets/svgs/figma.svg"
              alt="Figma SVG"
              style="width: 30px; height: 50px; margin-right: 10px"
            />
          </a>

          <a href="https://www.adobe.com/products/xd.html" target="_blank">
           <img
            src="../assets/svgs/adobeXd.svg"
            alt="Adobe Xd SVG"
            style="width: 30px; height: 50px"
          />
          </a>

         
        </MDBCol>

        <MDBCol col="4" style="padding: 15px">
          <p>Back-end</p>

          <a href="https://www.mongodb.com" target="_blank">
            <img
              src="../assets/svgs/mongoDB.svg"
              alt="MongoDB SVG"
              style="
                width: 30px;
                height: 40px;
                margin-right: 10px;
                margin-bottom: 10px;
              "
            />
          </a>
          <a href="https://nodejs.org" target="_blank">
           <img
            src="../assets/svgs/node.svg"
            alt="node SVG"
            style="width: 30px; height: 50px"
          />
          </a>
         
        </MDBCol>
      </MDBRow>
    </MDBCol>
  </MDBRow>
</template>

<script>
import { MDBCol, MDBRow } from "mdb-vue-ui-kit";
export default {
  components: {
    MDBCol,
    MDBRow,
  },
};
</script>

<style scoped>
p {
  color: #a28fca;
}
a {
  color: #7055a0;
  padding-right: 0px;
  padding-left: 0px;
}
</style>