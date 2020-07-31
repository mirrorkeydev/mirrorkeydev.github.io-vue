<template>
  <div class="projects">
    <SecondaryHeader subtitle="projects"/>
    <div class="main-container">
        <div class="sub-container">
          <h3>code</h3>
          <p>asdfasd</p>
        </div>
        <div class="sub-container">
          <h3>renders</h3>
          <p>asdfasd</p>
        </div>
        <div class="sub-container">
          <h3>art</h3>
          <p>asdfasd</p>
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

<style lang="scss">

h3 {
  background-color: white;
  bottom: 3vw;
  display: inline-block;
  font-size: 3vw;
  margin: 0;
  padding: 0 15px;
  position: relative;
}

p {
  text-align: left;
  margin: 0;
}

.projects
{
  background-color: white;
}

.main-container {
  display: flex;
  flex-wrap: wrap;
  font-style: 'Roboto', sans-serif;
  justify-content: center;
  margin: 5vw;
}

.sub-container {
  border: 1px solid rgb(228, 228, 228);
  border-radius: 5px;
  flex: 1 1 400px;
  padding: 10px;
  margin: 4vw;
}

/* Screens < 500px wide */
@media screen and (max-width: 500px) {
  h3 {
    bottom: 5.5vw;
    font-size: 5vw;
  }
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  h3 {
    bottom: 2vw;
    font-size: 2vw;
  }

  .sub-container {
    margin: 2vw;
  }
}

/* Screens > 1700px wide */
@media screen and (min-width: 1700px) {
  h3 {
    bottom: 1.25vw;
    font-size: 1.25vw;
  }
}

</style>
