<template>
  <div class="home">
    <video autoplay loop muted playsinline>
      <source src="../assets/Done-2.mp4" type="video/mp4">
    </video>
    <nav id="nav-container">
      <router-link to="" class="nav-link">about</router-link>
      <router-link to="" class="nav-link">projects</router-link>
      <router-link to="" class="nav-link">contact</router-link>
    </nav>
    <h1 id="title" class="unselectable">melanie<br>gutzmann</h1>
  </div>
</template>

<script>
export default {
  name: 'Home',
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

#nav-container
{
  color: white;
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  line-height: 13vw;
  padding: 5vw;
  position: fixed;
  right: 5vw;
  z-index: 1;
}
#title
{
  align-items: flex-end;
  box-sizing: border-box;
  color: white;
  display: flex;
  font-family: 'Rubik', sans-serif;
  font-size: 15vw;
  height: 100%;
  justify-content: left;
  line-height: 13vw;
  margin: 0;
  padding: 10vw;
  position: relative;
  text-align: left;
}
.home
{
  height: 100%;
}
.nav-link
{
  color: white;
  font-size: 3vw;
  padding: 0 1vw;
  text-decoration: none;
}
video
{
  border: white 5vw solid;
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
