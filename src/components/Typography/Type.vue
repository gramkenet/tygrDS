<template>
  <component
    :is="component"
    :class="component">
    <slot />
  </component>
</template>

<script>
export default {
  name: 'tygr-type',
  props: {
    component: {
      type: String,
      default: 'span'
    }
  }
}
</script>
<style lang="scss" scoped>
  @import '../../styles/tokens.scss';

  * {
    font-family: $ff_fallback;

    .wf-active & {
      font-family: $ff_primary;
    }
  }

  h1, .h1, h2, .h2, h3, .h3, h4, .h4, h5, .h5, h6, .h6 {
    font-weight: $fw_default;

    &.strong {
      font-weight: $fw_bold;
    }
  }

  h1, .h1 {
    font-size: $fs9;
  }

  h2, .h2 {
    font-size: $fs7;
  }

  h3, .h3 {
    font-size: $fs6;
  }

  h4, .h4 {
    font-size: $fs5;
  }

  h5, .h5 {
    font-size: $fs4;
  }

  h6, .h6 {
    font-size: $fs3;
  }

  p, span {
    font-weight: $fw_default;

    &.strong {
      font-weight: $fw_bold;
    }
  }
</style>
