<template>
  <div id="app">
    <h2 class="header"><span>Transparency</span> <AiProtocolsSquare /></h2>
    <h5>Tracking Security Metrics Across RBC</h5>
    <Spacer />
    <AttackList :attacks="attacks" />
  </div>
</template>

<script>
import { AiProtocolsSquare } from '@kalimahapps/vue-icons/ai';
import AttackList from './components/AttackList.vue';
import Spacer from './components/Spacer.vue';
import attacks from './data/attacks.json';

export default {
  name: 'App',
  data() {
    return {
      attacks: attacks.data,
    };
  },
  components: {
    AttackList,
    AiProtocolsSquare,
    Spacer,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.header > span {
  margin-right: 5px;
}
</style>
