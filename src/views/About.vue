<template>
  <div class="about">
    <SecondaryHeader subtitle="about"/>
    <div class="main-container">
      <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo. Quisque sit amet est et sapien ullamcorper pharetra. Vestibulum erat wisi, condimentum sed, commodo vitae, ornare sit amet, wisi. Aenean fermentum, elit eget tincidunt condimentum, eros ipsum rutrum orci, sagittis tempus lacus enim ac dui. Donec non enim in turpis pulvinar facilisis. Ut felis. Praesent dapibus, neque id cursus faucibus, tortor neque egestas augue, eu vulputate magna eros eu erat. Aliquam erat volutpat. Nam dui mi, tincidunt quis, accumsan porttitor, facilisis luctus, metus</p>
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
  font-style: 'Roboto', sans-serif;
  margin: 5vw;
}

/* Screens > 1000px wide */
@media screen and (min-width: 1000px) {

}

/* Screens > 2000px wide */
@media screen and (min-width: 2000px) {

}

</style>
