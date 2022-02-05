<template>
  <div :class="[
    'tygr-grid',
    cols && `tygr-grid-col-size-${cols}`,
    bp1 && `tygr-grid-bp1-col-${bp1}`,
    bp2 && `tygr-grid-bp2-col-${bp2}`,
    bp3 && `tygr-grid-bp3-col-${bp3}`,
    bp4 && `tygr-grid-bp4-col-${bp4}`,
    bp5 && `tygr-grid-bp5-col-${bp5}`,
    `tygr-grid-row-size-${rows}`,
    `tygr-grid-gap-size-${gap}`
  ]">
      <slot />
  </div>
</template>

<script>
export default {
  name: 'tygr-grid',
  props: {
    cols: String,
    bp1: String,
    bp2: String,
    bp3: String,
    bp4: String,
    bp5: String,
    gap: String,
    rows: String
  }
}
</script>
<style lang="scss" scoped>
  @import '../styles/tokens.scss';

  $sizes: $sm2, $sm3, $sm4, $sm5, $md1, $md2;

  .tygr-grid {
    display: grid;

    @for $i from 1 through length($sizes) {
      &-gap-size {
        &-#{$i} {
          grid-gap: nth($sizes, $i);
        }
      }
    }
    @for $i from 1 through 12 {
      &-col-size {
        &-#{$i} {
          grid-template-columns: repeat($i, 1fr);
        }
      }
      &-row-size {
        &-#{$i} {
          grid-template-rows: repeat($i, 1fr);
        }
      }
    }

    &-bp1-col {
      @for $i from 1 through 12 {
        &-#{$i} {
          @media screen and (max-width: $bp2) {
            grid-template-columns: repeat($i, 1fr)
          }
        }
      }
    }

    &-bp2-col {
      @for $i from 1 through 12 {
        &-#{$i} {
          @media screen and (min-width: $bp2) {
            grid-template-columns: repeat($i, 1fr)
          }
        }
      }
    }

    &-bp3-col {
      @for $i from 1 through 12 {
        &-#{$i} {
          @media screen and (min-width: $bp3) {
            grid-template-columns: repeat($i, 1fr)
          }
        }
      }
    }

    &-bp4-col {
      @for $i from 1 through 12 {
        &-#{$i} {
          @media screen and (min-width: $bp4) {
            grid-template-columns: repeat($i, 1fr)
          }
        }
      }
    }

    &-bp5-col {
      @for $i from 1 through 12 {
        &-#{$i} {
          @media screen and (min-width: $bp5) {
            grid-template-columns: repeat($i, 1fr)
          }
        }
      }
    }
  }
</style>
