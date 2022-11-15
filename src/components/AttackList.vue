<template>
  <h4 class="attack-list-header">Attack List</h4>
  <Divider />
  <Spacer />
  <div class="attack-list">
    <AttackListing v-for="attack in attacks" :attack="attack" />
  </div>
</template>

<script>
import AttackListing from './AttackListing.vue'
import Divider from './Divider.vue';
import Spacer from './Spacer.vue'
export default {
  name: 'AttackList',
  props: {
    attacks: Array<Object>,
  },
  components: {
    Divider,
    AttackListing,
    Spacer
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.attack-list-header {
  margin-bottom: 8px;
}

.attack-list {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-height: 100%;
  overflow: hidden;
}
</style>
