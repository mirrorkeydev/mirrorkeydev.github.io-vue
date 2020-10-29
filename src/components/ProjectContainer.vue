<template>
  <div class="project-container">
    <img class="project-img" :src="require(`@/assets/${imgsrc}`)" alt="">
    <div class="project-text">
      <p class="strong">
        {{ title }}
        <span v-if="github.length" class="right">(<a :href="github" target="_blank" rel="noopener noreferrer">GitHub</a>)</span>
        <span v-if="site.length" class="right">(<a :href="site" target="_blank" rel="noopener noreferrer">Site</a>) </span>
      </p>
      <p>{{ subtitle }}</p>
      <p class="main">
        <slot></slot>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectContainer',
  props: {
    title: String,
    subtitle: String,
    imgsrc: String,
    site: String,
    github: String
  }
};
</script>

<style scoped lang="scss">
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

.project-container {
  border: 1px solid rgb(216, 216, 216);
  border-radius: 5px;
  margin: 2vw 0 3vw 0;
  padding: 5vw 5vw 0 5vw;
}

a {
  color: rgb(0, 144, 137);
  font-weight: 500;
  text-decoration: none;
  border-bottom: 2px solid rgba(0, 144, 137, 0.411);
}

p {
  margin: 0;
}

p.strong {
  margin: 0 0 5px 0;
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

/* Screens < 500px wide */
@media screen and (max-width: 500px) {
  .project-text {
    font-size: 3vw;
  }
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {
  .project-text {
    font-size: 1.2vw;
    margin: 2vw 0;
    text-align: left;
  }

  .project-container {
    margin: 2vw 0 3vw 0;
    padding: 2vw 2vw 0 2vw;
  }

  .project-text.buffered {
    margin: 1.75vw;
  }
}

/* Screens > 1700px wide */
@media screen and (min-width: 1700px) {
  .project-text {
    font-size: 0.8vw;
    margin: 1.5vw 0;
    text-align: left;
  }

  .project-container {
    margin: 1vw 0 1.5vw 0;
    padding: 1.5vw 1.5vw 0 1.5vw;
  }

  .project-text.buffered {
    margin: 1.5vw;
  }
}
</style>
