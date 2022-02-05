<template>
  <div class="tygr-home">
    <!-- Default Cards -->
    <tygr-card title="Default Cards" context="documentation" class="tygr-home-info">
      <template v-slot:body>
        <tygr-grid bp1="1" bp2="2" bp3="3" bp4="4" gap="4">
          <tygr-card
            v-for="(card, index) in cards"
            :key="index"
            :title="`No Image ${index + 1}`"
            :subtitle="`Secondary text ${index + 1}`">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
        </tygr-grid>
      </template>
    </tygr-card>
    <!-- Default Cards with Image -->
    <tygr-card title="Default Cards with Image" context="documentation" class="tygr-home-info">
      <template v-slot:body>
        <tygr-grid bp1="1" bp2="2" bp3="3" bp4="4" gap="4">
          <tygr-card
            v-for="(card, index) in cards"
            :key="index"
            :title="`Vertical ${index + 1}`"
            subtitle="Secondary text">
            <template v-slot:image>
              <img src="../assets/tiger-sm.jpg" alt="Image of tiger" />
            </template>
            <template v-slot:body>
              <p v-html="card.bodyContent" />
            </template>
          </tygr-card>
        </tygr-grid>
      </template>
    </tygr-card>
    <!-- Horizontal Cards -->
    <tygr-card title="Horizontal Cards" context="documentation" class="tygr-home-info">
      <template v-slot:body>
        <tygr-grid bp1="1" bp4="2" rows="2" gap="4">
          <tygr-card-horizontal
            v-for="(card, index) in cards"
            :key="index"
            :title="`Horizontal ${index + 1}`">
            <template v-slot:image>
              <img src="../assets/tiger-sm.jpg" alt="Image of tiger" />
            </template>
            <template v-slot:body>
              <p v-html="card.bodyContent" />
            </template>
          </tygr-card-horizontal>
        </tygr-grid>
      </template>
    </tygr-card>
    <!-- Context -->
    <tygr-card title="Context" context="documentation" class="tygr-home-info">
      <template v-slot:body>
        <tygr-grid bp1="1" bp2="2" bp3="3" bp4="4" gap="4">
          <!-- Primary -->
          <tygr-card
            title="Primary"
            subtitle="Secondary text"
            context="primary">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Secondary -->
          <tygr-card
            title="Secondary"
            subtitle="Secondary text"
            context="secondary">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Success -->
          <tygr-card
            title="Success"
            subtitle="Secondary text"
            context="success">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Light -->
          <tygr-card
            title="Light"
            subtitle="Secondary text"
            context="light">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Dark -->
          <tygr-card
            title="Dark"
            subtitle="Secondary text"
            context="dark">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Info -->
          <tygr-card
            title="Info"
            subtitle="Secondary text"
            context="info">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Warning -->
          <tygr-card
            title="Warning"
            subtitle="Secondary text"
            context="warning">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
          <!-- Severe -->
          <tygr-card
            title="Severe"
            subtitle="Secondary text"
            context="severe">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
            <template v-slot:footer>
              <p v-html="cards[0].footerContent" />
            </template>
          </tygr-card>
        </tygr-grid>
      </template>
    </tygr-card>
    <!-- Context Horizontal -->
    <tygr-card title="Context Horizontal" context="documentation" class="tygr-home-info">
      <template v-slot:body>
        <tygr-grid bp1="1" bp3="2" bp4="3" gap="4">
          <!-- Primary -->
          <tygr-card-horizontal
            title="Primary"
            subtitle="Secondary text"
            context="primary">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Secondary -->
          <tygr-card-horizontal
            title="Secondary"
            subtitle="Secondary text"
            context="secondary">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Success -->
          <tygr-card-horizontal
            title="Success"
            subtitle="Secondary text"
            context="success">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Light -->
          <tygr-card-horizontal
            title="Light"
            subtitle="Secondary text"
            context="light">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Dark -->
          <tygr-card-horizontal
            title="Dark"
            subtitle="Secondary text"
            context="dark">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Info -->
          <tygr-card-horizontal
            title="Info"
            subtitle="Secondary text"
            context="info">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Warning -->
          <tygr-card-horizontal
            title="Warning"
            subtitle="Secondary text"
            context="warning">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
          <!-- Severe -->
          <tygr-card-horizontal
            title="Severe"
            subtitle="Secondary text"
            context="severe">
            <template v-slot:body>
              <p v-html="cards[0].bodyContent" />
            </template>
          </tygr-card-horizontal>
        </tygr-grid>
      </template>
    </tygr-card>
  </div>
</template>

<script>
import tygrGrid from './Grid.vue';
import tygrCard from './Card/Card';
import tygrCardHorizontal from './Card/CardHorizontal';

export default {
  name: 'tygr-home',
  components: {
    tygrGrid,
    tygrCard,
    tygrCardHorizontal
  },
  props: {
    msg: String
  },
  data () {
    return {
      cards: [
        {
          bodyContent: "Body Content 1",
          footerContent: "Footer Content 1"
        },
        {
          bodyContent: "Body Content 2",
          footerContent: "Footer Content 2"
        },
        {
          bodyContent: "Body Content 3",
          footerContent: "Footer Content 3"
        },
        {
          bodyContent: "Body Content 4",
          footerContent: "Footer Content 4"
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
@import '../styles/tokens.scss';

.tygr-home {
  margin-top: $md3;

  &-info {
    margin-bottom: $md3;
  }

  .tygr-grid {
    margin: $md2;
  }
}
</style>
