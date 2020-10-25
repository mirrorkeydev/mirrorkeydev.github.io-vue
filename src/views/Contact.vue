<template>
  <div class="contact">
    <SecondaryHeader subtitle="contact"/>
    <div class="main-container">
      <div>
        <div><a href="mailto:mirrorkeydev@gmail.com"><span></span>mirrorkeydev<span>@gmail.com</span></a></div>
        <div><a href="https://github.com/mirrorkeydev"><span>github.com/</span>mirrorkeydev<span></span></a></div>
        <div><a href="https://discord.com/"><span></span>mirrorkeydev<span>#0120</span></a></div>
        <div><a href="https://www.linkedin.com/in/mirrorkeydev/"><span>linkedin.com/in/</span>mirrorkeydev<span></span></a></div>
      </div>
    </div>
  </div>
</template>

<script>
import SecondaryHeader from '../components/SecondaryHeader.vue';

export default {
  name: 'Contact',
  components: {
    SecondaryHeader: SecondaryHeader
  }
};
</script>

<style lang="scss">

.projects
{
  background-color: white;
}

.main-container {
  color: rgb(129, 129, 129);
  font-family: "Roboto", sans-serif;
  font-weight: 500;
  font-size: calc(max(3vh, 20px));
  line-height: 3rem;
  padding-top: 15vh;
  text-align: center;
}

.main-container span {
  color: rgb(49, 49, 49);
  font-weight: 600;
}

.main-container span:first-of-type {
  text-align:right
}

.main-container {
  font-style: 'Roboto', sans-serif;
  margin: 5vw;
}

a {
  color: rgb(129, 129, 129);
  text-decoration: none;
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .main-container {
    font-size: 2.5rem;
    line-height: 4rem;
    padding-top: 10%;
    text-align: center;
  }

  .main-container span {
    width: 300px;
    display: inline-block;
    text-align: left;
  }
}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {
  .main-container {
    font-size: 2.5rem;
    line-height: 4rem;
    padding-top: 10%;
    text-align: center;
  }

  .main-container span {
    width: 300px;
    display: inline-block;
    text-align: left;
  }
}

</style>
