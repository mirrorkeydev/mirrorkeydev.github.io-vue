<template>
  <div class="about">
    <SecondaryHeader subtitle="about"/>
    <div class="main-container">
      <p>
        Hello! My name is Melanie, and I'm a junior at Oregon State University
        studying CS. During the school year, I work at OSU's Center for Applied
        Systems and Software, writing software for the
        Oregon Department of Transportation and the Linux Foundation. Last summer
        I was a STEP intern at Google, and I'm currently looking for summer 2021
        opportunities.
      </p>
    </div>
  </div>
</template>

<script>
import SecondaryHeader from '../components/SecondaryHeader.vue';

export default {
  name: 'About',
  components: {
    SecondaryHeader: SecondaryHeader
  }
};
</script>

<style lang="scss">

.about
{
  background-color: white;
}

.main-container {
  color: rgb(129, 129, 129);
  font-family: "Roboto", sans-serif;
  font-weight: 500;
  font-size: calc(max(3vh, 20px));
  line-height: 2rem;
  margin: 4vw 7vw;
  text-align: left;
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .main-container {
    margin: 4vw 10vw;
    line-height: 3rem;
  }
}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {
  .main-container {
    margin: 4vw 20vw;
    line-height: 3rem;
  }
}

</style>
