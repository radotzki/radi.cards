<template>
  <div class="container">
    <h1 style=" margin-bottom:10px;">Artwork Gallery</h1>
    <p>Creative, unique art pieces from from all around the interwebs.</p>
    <b-row class="text-center">
      <div v-for="card in cards" :key="card.tokenId">
        <b-col cols="6">
          <card :cdata="card"/>
        </b-col>
      </div>
    </b-row>
  </div>
</template>

<script>
import { mapState } from "vuex";
import Card from "../../components/widgets/Card";

export default {
  name: "creator",
  components: { Card },
  data() {
    return {};
  },
  computed: {
    ...mapState(["cards"])
  },
  mounted() {
    this.$nextTick(function() {});
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
@import "../../styles/variables.scss";
.card-selected {
  margin-top: -25px;
  transition: all 0.2s ease-in-out;
}
</style>
