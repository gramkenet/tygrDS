<template>
  <tygr-card-base :class="context && `context ${context}`">
    <template v-slot:image>
      <slot name="image" />
    </template>
    <template v-slot:header>
      <tygr-type
        v-if="title"
        component="h4"
        class="tygr-card-header-title">
        {{ title }}
      </tygr-type>
      <tygr-type
        v-if="subtitle"
        component="p"
        class="tygr-card-header-subtitle">
        {{ subtitle }}
      </tygr-type>
    </template>
    <template v-slot:body>
      <slot name="body" />
    </template>
    <template v-slot:footer>
      <slot name="footer" />
    </template>
  </tygr-card-base>
</template>

<script>
import tygrCardBase from './_Card';
import tygrType from  '../Typography/Type';

export default {
  name: 'tygr-card',
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
    &.context {
      .tygr-card-header {
        padding-top: $sm4;
        border-top-left-radius: $sm2;
        border-top-right-radius: $sm2;

        &-title {
          margin: 0;
        }
      }
    }

    &.documentation {
      text-align: left;
      background-color: $clr_neutral1;
      box-shadow: none;
      border: none;

      .tygr-card-header {
        &-title {
          margin-bottom: $sm4;
        }
      }
    }

    &.primary {
      .tygr-card-header {
        background-color: $clr_blue_gray7;
        color: $clr_white;
      }
    }

    &.secondary {
      .tygr-card-header {
        background-color: $clr_neutral4;
      }
    }

    &.success {
      border-color: $clr_green1;

      .tygr-card-header {
        background-color: $clr_green1;
      }
    }

    &.light {
      border: none;
      background-color: $clr_white;
    }

    &.dark {
      border-color: $clr_neutral9;

      .tygr-card-header {
        background-color: $clr_neutral9;
        color: $clr_neutral1;
      }
    }

    &.info {
      border-color: $clr_blue7;

      .tygr-card-header {
        background-color: $clr_blue7;
        color: $clr_neutral1;
      }
    }

    &.warning {
      border-color: $clr_orange1;

      .tygr-card-header {
        background-color: $clr_orange1;
      }
    }

    &.severe {
      border-color: $clr_red4;

      .tygr-card-header {
        background-color: $clr_red4;
        color: $clr_neutral1;
      }
    }
  }
</style>
