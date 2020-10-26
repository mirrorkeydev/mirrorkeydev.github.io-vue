<template>
  <div class="projects">
    <SecondaryHeader on="projects"/>
    <div class="projects-container">
        <div class="sub-container">
          <h3>code</h3>
          <div class="inside-container">
            <div>
              <img class="project-img" src="@/assets/sprout.png" alt="">
              <p>
                A dashboard that shows real-time statistics about my plants and their
                environment. Offers soil moisture charts for each plant connected to
                Sprout and environmental statistics about the plants' environment,
                including temperature/humidity. Plus, it's pretty cute.
              </p>
              <img class="project-img" src="@/assets/noms.png" alt="">
              <img class="project-img" src="@/assets/mathlang.png" alt="">
              <img class="project-img" src="@/assets/visualizations.png" alt="">
              <img class="project-img" src="@/assets/catspot.png" alt="">
              <img class="project-img" src="@/assets/appstract.png" alt="">
            </div>
          </div>
        </div>
        <div class="sub-container">
          <h3>renders</h3>
          <div class="inside-container">
            <p>asdfasd</p>
          </div>
        </div>
        <div class="sub-container">
          <h3>art</h3>
          <div class="inside-container">
            <p>asdfasd</p>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import SecondaryHeader from '../components/SecondaryHeader.vue';

export default {
  name: 'Projects',
  components: {
    SecondaryHeader: SecondaryHeader
  }
};
</script>

<style lang="scss" scoped>

h3 {
  background-color: white;
  color: rgb(85, 85, 85);
  display: inline-block;
  font-size: 5vw;
  margin: 0;
  padding: 0 15px;
  position: relative;
  top: 2vw;
}

p {
  text-align: left;
  margin: 0;
}

.project-img {
  width: 100%;
}

.project-title {
  font-size: 2vw;
}

.projects
{
  background-color: white;
}

.projects-container {
  align-items: stretch;
  display: flex;
  flex-wrap: wrap;
  font-style: 'Roboto', sans-serif;
  justify-content: center;
  margin: 5vw;
}

.sub-container {
  flex: 1 1 400px;
  margin: 4vw;
}

.inside-container {
  border: 1px solid rgb(228, 228, 228);
  border-radius: 5px;
  padding: 2vw;
}

/* Screens < 500px wide */
@media screen and (max-width: 500px) {
  h3 {
    font-size: 6vw;
    top: 3vw;
  }
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .sub-container {
    margin: 2vw;
  }

  h3 {
    font-size: 2vw;
    top: 1vw;
  }
}

/* Screens > 1700px wide */
@media screen and (min-width: 1700px) {
}

</style>
