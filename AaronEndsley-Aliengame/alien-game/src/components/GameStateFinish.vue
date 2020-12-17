<template>
  <div>
    <div class="modal">
      <h2 v-if="uiState === 'lost'">You Lost</h2>
      <h2 v-else-if="uiState === 'won'">You Won</h2>
      <Face />
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
import Face from '../components/Face';

export default {
  components: {
    Face,
  },
  computed: {
    ...mapState(['uiState']),
  },
};
</script>

<style lang="scss" scoped></style>
