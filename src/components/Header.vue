<template>
  <tygr-type
    component="div"
    class="tygr-header">
    <img
      alt="Tygr Design System"
      src="../assets/tygr-sm.jpg"
      class="tygr-header-image">
    <tygr-type
      component="h1"
      class="tygr-header-title strong">
      {{ title }}
    </tygr-type>
  </tygr-type>
</template>

<script>
import tygrType from './Typography/Type';

export default {
  name: 'tygr-header',
  components: {
    tygrType
  },
  props: {
    title: String
  }
}
</script>
<style lang="scss" scoped>
@import '../styles/tokens.scss';

.tygr-header {
  display: flex;

  &-title {
    margin: 0;
    align-self: center;
  }
}
</style>
