<template>
  <div class="secondary-header">
    <router-link :to="{ name: '/landing' }">
      <h1 id="header-title" class="unselectable">
        melanie gutzmann
      </h1>
    </router-link>
    <h1 class="unselectable">• {{ subtitle }}</h1>
  </div>
</template>

<script>
export default {
  name: 'SecondaryHeader',
  props: {
    subtitle: String
  }
};
</script>

<style scoped lang="scss">

.secondary-header {
  margin: 4vw 5vw;
  text-align: left;
}

#header-title {
  animation: GradientShift 4s ease infinite;
  -moz-animation: GradientShift 4s ease infinite;
  -webkit-animation: GradientShift 4s ease infinite;
  -webkit-background-clip: text;
  background-image: linear-gradient(104deg, #049bb0, #a5bb43);
  background-size: 200% 200%;
  color: var(--placeholder-green);
  margin: 0 1vw 0 0;
  -webkit-text-fill-color: transparent;
}

h1 {
  display: inline-block;
  font-family: 'Rubik', sans-serif;
  font-size: 5vw;
  margin: 0;
}

a {
  text-decoration: none;
}

a:hover {
  cursor: pointer;
}

@-webkit-keyframes GradientShift {
  0%{background-position:0% 65%}
  50%{background-position:100% 36%}
  100%{background-position:0% 65%}
}
@-moz-keyframes GradientShift {
  0%{background-position:0% 65%}
  50%{background-position:100% 36%}
  100%{background-position:0% 65%}
}
@keyframes GradientShift {
  0%{background-position:0% 65%}
  50%{background-position:100% 36%}
  100%{background-position:0% 65%}
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .secondary-header {
    margin: 2vw 3vw;
  }

  h1 {
    font-size: 3vw;
  }
}

/* Screens < 600px wide */
@media screen and (max-width: 600px) {
  .secondary-header {
    margin: 5vw 7vw;
  }

  h1 {
    font-size: 10vw;
  }
}

</style>
