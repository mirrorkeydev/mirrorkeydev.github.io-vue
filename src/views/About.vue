<template>
  <div class="about">
    <SecondaryHeader on="about"/>
    <div class="about-container">
      <p>
        Hello! My name is Melanie, and I'm a junior at Oregon State University
        studying CS. During the school year, I work at OSU's Center for Applied
        Systems and Software, writing software for the
        Oregon Department of Transportation and the Linux Foundation. Last summer
        I was a STEP intern at Google, and I'm currently looking for summer 2021
        opportunities.
      </p>
      <p>
        In my free time, I like taking care of my houseplants, attempting art, mending my
        possessions, and low-stakes hiking.
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

<style lang="scss" scoped>

.about
{
  background-color: white;
}

.about-container {
  color: rgb(129, 129, 129);
  font-family: "Roboto", sans-serif;
  font-weight: 500;
  font-size: calc(max(3vh, 20px));
  line-height: calc(max(3vh, 1.5rem));
  margin: 4vw 7vw;
  text-align: left;
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .about-container {
    margin: 7vw 10vw;
    line-height: normal;
  }
}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {
  .about-container {
    margin: 10vw 20vw;
    line-height: normal;
  }
}

</style>
