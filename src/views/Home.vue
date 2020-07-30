<template>
  <div class="home">
    <video autoplay loop muted>
      <source src="../assets/Done-2.mp4" type="video/mp4">
    </video>
    <h1 id="title">melanie</h1>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@700&display=swap');
#title {
  color: white;
  font-size: 15vw;
  font-family: 'Rubik', sans-serif;
  position: relative;
  height: 100vh;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  padding: 0;
  user-select: none;
  -moz-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  -o-user-select: none;
}

video {
  object-fit: cover;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  box-sizing: border-box;
  border: white 5vw solid;
  margin: 0;
}

</style>
