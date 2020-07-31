<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script>
export default {
  name: 'About',
  methods: {
    mounted () {
      // Workaround to correctly set the viewheight on mobile
      const vh = window.innerHeight * 0.01;
      document.documentElement.style.setProperty('--vh', `${vh}px`);
    }
  }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');

.about
{
  border: black 5vw solid;
  box-sizing: border-box;
  height: calc(100vh - calc(100vh - 100%));
  left: 0;
  margin: 0;
  object-fit: cover;
  position: fixed;
  top: 0;
  width: 100vw;
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  #title {
    font-size: 10vw;
    line-height: 10vw;
  }

  .nav-link {
    font-size: 2vw;
  }

  #nav-container {
    padding: 4vw;
  }
}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {
  #title {
    font-size: 7vw;
    line-height: 7vw;
  }

  .nav-link {
    font-size: 1vw;
  }

  #nav-container {
    padding: 2vw;
  }
}

</style>
