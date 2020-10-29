<template>
  <div class="projects">
    <SecondaryHeader on="projects"/>
    <div class="projects-container">
        <div class="sub-container">
          <h3>code</h3>
          <div class="inside-container">
            <ProjectContainer title="Sprout" subtitle="Personal Project, June 2020" imgsrc="sprout.png"
              site="https://mirrorkey.dev/Sprout" github="https://github.com/mirrorkeydev/Sprout">
              A dashboard that shows real-time statistics about my
              plants and their environment. Offers soil moisture charts for each plant connected
              to Sprout and environmental statistics about the plants' environment,
              including temperature/humidity. Plus, it's pretty cute.
            </ProjectContainer>
            <ProjectContainer title="noms" subtitle="Google STEP Internship Capstone, Summer 2020" imgsrc="noms.png"
                site="" github="https://github.com/googleinterns/noms">
              A full-stack web app connecting students and college organizations
              to battle food insecurity and food waste. noms allows college organizations to post the
              locations of free food on campus and for students to view and receive notifications for
              these posts.
            </ProjectContainer>
            <ProjectContainer title="MathLang" subtitle="Programming Language Fundamentals Final, March 2020" imgsrc="mathlang.png"
                site="" github="https://github.com/mirrorkeydev/MathLang">
              A stack-based language that performs basic mathematic/logic operations.
              Values include integers, doubles, booleans, tuples, commands, and functions.
              Can perform basic operations on values and allows conditional logic such as if/else
              statements and while/for loops. Interpreter written in Haskell.
            </ProjectContainer>
            <ProjectContainer title="Visualizations" subtitle="Personal Project, February 2020" imgsrc="visualizations.png"
                site="https://mirrorkey.dev/Visualizations" github="https://github.com/mirrorkeydev/Visualizations">
              Various visualizations created as an exercise in data processing.
              Includes interactive charts and original infographics, exploring
              data such as my Netflix binges and the patterns of texts to a friend.
            </ProjectContainer>
            <ProjectContainer title="CatSpot" subtitle="Web Development Final, December 2019" imgsrc="catspot.png"
                site="" github="https://github.com/mirrorkeydev/CatSpot">
              A web app that allows students to track cat spottings on campus.
              Cats can be given names and assigned pictures, energy levels, sociability status,
              and a recent location. The interactive map shows cat spottings in the last 24 hours.
            </ProjectContainer>
            <ProjectContainer title="Appstract" subtitle="Personal Project, March 2019" imgsrc="appstract.png"
                site="https://play.google.com/store/apps/details?id=com.melon.appstract&hl=en_US" github="https://github.com/mirrorkeydev/Appstract">
              An artistically abstract Android icon pack. 300+ icons supported across 25+ launchers.
              Built on the open source CandyBar dashboard. Available on the Google Play Store.
            </ProjectContainer>
          </div>
        </div>
        <div class="sub-container">
          <h3>renders</h3>
          <div class="inside-container">
            <div class="project-container">
              <video class="project-img" autoplay loop muted playsinline>
                <source src="../assets/desktop-background.mp4" type="video/mp4">
              </video>
              <div class="project-text buffered">
                <p class="left strong">Iridescent Wave</p><p class="right">April 2020</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/rope8.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Coil</p><p class="right">March 2020</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/tile3.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Bounce</p><p class="right">September 2019</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/glassy5.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Glassy</p><p class="right">June 2019</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/room5.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Suede</p><p class="right">September 2018</p>
              </div>
            </div>
          </div>
        </div>
        <div class="sub-container">
          <h3>art</h3>
          <div class="inside-container">
            <div class="project-container">
              <img class="project-img" src="@/assets/octopus.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Minoa</p><p class="right">September 2020</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/maroon.png" alt="">
              <div class="project-text buffered">
                <p class="left strong">Peach</p><p class="right">September 2020</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/lamy.jpg" alt="">
              <div class="project-text buffered">
                <p class="left strong">Lamy Safari</p><p class="right">March 2020</p>
              </div>
            </div>
            <div class="project-container">
              <img class="project-img" src="@/assets/hills.jpg" alt="">
              <div class="project-text buffered">
                <p class="left strong">Hills</p><p class="right">January 2020</p>
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import SecondaryHeader from '../components/SecondaryHeader.vue';
import ProjectContainer from '../components/ProjectContainer.vue';

export default {
  name: 'Projects',
  components: {
    SecondaryHeader: SecondaryHeader,
    ProjectContainer: ProjectContainer
  }
};
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

a {
  color: green;
  text-decoration: none;
}

.strong {
  color: rgb(78, 78, 78);
  font-weight: 600;
}

.left {
  float: left;
  margin: 0 0 0 0.5vw;
}

.right {
  float: right;
  margin: 0 0.5vw 0 0;
}

.main::before {
  content: "\A";
  white-space: pre;
}

p {
  margin: 0;
}

h3 {
  background-color: white;
  color: rgb(85, 85, 85);
  display: block;
  font-size: 4vw;
  margin: 0;
  text-align: center;
}

.project-text {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-size: 2.5vw;
  margin: 4vw 0;
  text-align: left;
  overflow: auto;
}

.project-img {
  border-radius: 5px;
  max-width: 100%;
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

.project-container {
  border: 1px solid rgb(216, 216, 216);
  border-radius: 5px;
  margin: 2vw 0 3vw 0;
  padding: 5vw 5vw 0 5vw;
}

.sub-container {
  flex: 1 1 400px;
  margin: 4vw;
}

.inside-container {
  padding: 2vw;
}

/* Screens < 500px wide */
@media screen and (max-width: 500px) {
  h3 {
    font-size: 6vw;
  }

  .project-text {
    font-size: 3vw;
  }

  .projects-container {
    margin: 0;
  }
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .sub-container {
    margin: 2vw;
  }

  h3 {
    font-size: 2.5vw;
  }

  .project-text {
    font-size: 1.2vw;
    margin: 2vw 0;
    text-align: left;
  }

  .project-container {
    margin: 2vw 0 3vw 0;
    padding: 2vw 2vw 0 2vw;
  }

  .inside-container {
    padding: 2vw 0;
  }

  .project-text.buffered {
    margin: 1.75vw;
  }
}

/* Screens > 1700px wide */
@media screen and (min-width: 1700px) {
  h3 {
    font-size: 1.8vw;
  }

  .project-text {
    font-size: 0.8vw;
    margin: 1.5vw 0;
    text-align: left;
  }

  .project-container {
    margin: 1vw 0 1.5vw 0;
    padding: 1.5vw 1.5vw 0 1.5vw;
  }

  .inside-container {
    padding: 2vw 0;
  }

  .project-text.buffered {
    margin: 1.5vw;
  }
}

</style>
