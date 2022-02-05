<template>
  <tygr-card-base
    :class="[
      'tygr-card-horizontal',
      !$slots.image && 'tygr-card-horizontal-text',
      context && `context ${context}`
    ]">
    <template v-if="$slots.image" class="tygr-card-horizontal-container" v-slot:image>
      <slot name="image" />
    </template>
    <template class="tygr-card-horizontal-container" v-slot:body>
      <slot name="header" />
      <tygr-type
        v-if="title"
        component="h3"
        class="tygr-card-header-title">
        {{ title }}
      </tygr-type>
      <tygr-type
        v-if="subtitle"
        component="p"
        class="tygr-card-header-subtitle">
        {{ subtitle }}
      </tygr-type>
      <slot name="body" />
      <slot name="footer" />
    </template>
  </tygr-card-base>
</template>

<script>
import tygrCardBase from './_Card';
import tygrType from  '../Typography/Type';

export default {
  name: 'tygr-card-horizontal',
  components: {
    tygrCardBase,
    tygrType
  },
  props: {
    context: String,
    image: String,
    subtitle: String,
    title: String
  }
}
</script>
<style lang="scss">
  @import '../../styles/tokens.scss';

  .tygr-card {
    &-horizontal {
      display: grid;
      grid-template-columns: 1fr 1fr;

      &-text {
        grid-template-columns: 1fr;
      }

      .tygr-card-body {
        .tygr-card-header-title {
          margin-top: $sm4;
        }
      }

      &.context {
        border: none;
        border-radius: $sm3;
      }

      &.primary {
        background-color: $clr_blue_gray7;
        color: $clr_white;
      }

      &.secondary {
        background-color: $clr_neutral4;
      }

      &.success {
        background-color: $clr_green1;
      }

      &.light {
        background-color: $clr_white;
      }

      &.dark {
        background-color: $clr_neutral9;
        color: $clr_neutral1;
      }

      &.info {
        background-color: $clr_blue7;
        color: $clr_neutral1;
      }

      &.warning {
        background-color: $clr_orange1;
      }

      &.severe {
        background-color: $clr_red4;
        color: $clr_neutral1;
      }
    }
  }
</style>
