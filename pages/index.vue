<template>
<page>
  <jumbotron-hero
    slot="masthead"
    bg-img-src="rohan-gangopadhyay-heIaYq6A7tg-unsplash.jpg"
    fluid
  />
  <div class="my-5 content" slot="content">

    <Section>
      <jumbotron-hero bg-img-src="/VESE-01.png" bg-color="grey" contain style="transform: translateY(-8rem)" />

    </Section>

    <Section>
      <b-jumbotron class="mb-5">
        <p>Expand the knowledge of students interested in vehicle electronics and systems engineering through hands on
          projects and close work with companies.</p>
        <divider />
        <p>Click the links below to learn more about VESE.</p>
        <b-button variant="primary" to="/about">About VESE</b-button>
        <b-button variant="secondary" to="#current-projects">Current Projects</b-button>
        <b-button variant="secondary" to="#current-projects">Gallery</b-button>
      </b-jumbotron>

    </Section>

    <divider />

    <Section>
      <h1 id="current-projects" class="d-flex justify-content-center mt-5">Current Projects</h1>
      <b-row class="mt-5" align-h="center">
        <b-card 
          v-for="(project, index) in projects" v-bind:key="index"
          :title="project.title"
          :img-src="project.imgsrc"
          style="max-width: 20rem;"
          class="m-2"
        >
          <b-card-text>{{ project.text }}</b-card-text>
          <b-button to="#">Read More</b-button>
        </b-card>
      </b-row>
    </Section>

  </div>
</page>
</template>

<script>
export default {
    data() {
      return {
        projects: [
          {
            "title": "FSAE Electric Vehicle",
            "imgsrc": "https://vese-uic.weebly.com/uploads/1/1/4/2/114284319/veseneon_orig.png",
            "text": "VESE is leading the push for developing, manufacturing and racing the first ever UIC FSAE Electric vehicle."
          },
          {
            "title": "Mechanical Team",
            "imgsrc": "https://vese-uic.weebly.com/uploads/1/1/4/2/114284319/tesla-ipad-3_orig.jpg",
            "text": "Mechanical Engineering students apply the information learned from class or on their own time to develop the systems of the FSAE Electric vehicle."
          },
          {
            "title": "Electrical team",
            "imgsrc": "https://vese-uic.weebly.com/uploads/1/1/4/2/114284319/ecu_orig.jpg",
            "text": "Electrical Engineering students developing the first ever electrical vehicle systems at UIC."
          }
        ]
      }
    }
}
</script>

<style>
.content {
    background-color: white;
}
</style>