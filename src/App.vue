<template>
  <tygr-header title="DS" />
  <tygr-home />
</template>

<script>
import tygrHeader from './components/Header.vue';
import tygrHome from './components/Home.vue';

export default {
  name: 'App',
  components: {
    tygrHeader,
    tygrHome
  }
}
</script>

<style lang="scss">
@import './styles/tokens.scss';
@import './styles/mixins/breakpoints.scss';

body {
  background-color: $clr_neutral1;
}

#app {
  font-family: $ff_fallback;
  color: $clr_neutral10;
  margin-top: $md4;
  max-width: 100%;
  margin: 0 auto;

  @include bp2 {
    max-width: 90%;
  }

  @include bp3 {
    max-width: 80%;
  }
}
</style>
