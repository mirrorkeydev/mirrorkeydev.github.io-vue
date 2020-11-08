<template>
  <div class="home">
    <video autoplay loop muted playsinline id="home-video" ref="homeVideo">
      <source src="../assets/desktop-background.mp4" type="video/mp4">
    </video>
    <nav id="nav-container">
      <router-link to="about" class="nav-link">about</router-link>
      <router-link to="projects" class="nav-link">projects</router-link>
      <router-link to="contact" class="nav-link">contact</router-link>
    </nav>
    <h1 id="title" class="unselectable">melanie<br>gutzmann</h1>
  </div>
</template>

<script>
export default {
  name: 'Home',
  mounted () {
    const vid = this.$refs.homeVideo;
    vid.style.opacity = 0;
    vid.oncanplay = () => {
      const vid = this.$refs.homeVideo;
      this.fadein(vid);
    };
  },
  methods: {
    fadein (element) {
      var op = 0;
      var timer = setInterval(() => {
        if (op >= 1) clearInterval(timer);
        element.style.opacity = op;
        element.style.filter = 'alpha(opacity=' + op * 100 + ')';
        op += op * 0.1 || 0.1;
      }, 50);
    }
  }
};
</script>

<style lang="scss" scoped>
#nav-container
{
  color: white;
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  padding: 10vw;
  position: fixed;
  right: 1vw;
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
  background-color: var(--placeholder-green);
  box-sizing: border-box;
  height: 100%;
}
.nav-link
{
  color: white;
  font-size: 4vw;
  padding: 0 1vw;
  text-decoration: none;
}
#home-video
{
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
    padding: 6vw;
  }
}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {
  #title {
    font-size: 7vw;
    line-height: 7vw;
    padding: 6vw;
  }

  .nav-link {
    font-size: 1vw;
  }

  #nav-container {
    padding: 4vw;
  }
}

</style>
