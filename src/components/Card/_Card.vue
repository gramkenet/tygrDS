<template>
  <div class="tygr-card">
    <div v-if="!isImageEmpty" class="tygr-card-image">
      <slot name="image" />
    </div>
    <div v-if="!isHeaderEmpty" class="tygr-card-header">
      <slot name="header" />
    </div>
    <div v-if="!isBodyEmpty" class="tygr-card-body">
      <slot name="body" />
    </div>
    <div v-if="!isFooterEmpty" class="tygr-card-footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'tygr-card-base',
  computed: {
    isImageEmpty () {
      return !this.$slots.image;
    },
    isHeaderEmpty () {
      return !this.$slots.header;
    },
    isBodyEmpty () {
      return !this.$slots.body;
    },
    isFooterEmpty () {
      return !this.$slots.footer;
    }
  }
}
</script>
<style lang="scss" scoped>
  @import '../../styles/tokens.scss';

  .tygr-card {
    background-color: $clr_neutral2;
    border: $xs1 solid $clr_neutral3;
    border-radius: $sm2;
    box-shadow: 0 $sm2 $sm4 hsl(0deg 0% 80% / 48%);
    text-align: center;

    &-image ::v-deep img {
      max-width: 100%;
      border-top-left-radius: $sm2;
      border-top-right-radius: $sm2;
    }

    &-header {
      border-bottom: $xs1 solid $clr_neutral3;
    }

    &-footer {
      border-top: 1px solid $clr_neutral3;
    }
  }
</style>
