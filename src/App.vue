<template>
  <div id="app">
    <h2 class="header"><span>Transparency</span> <AiProtocolsSquare /></h2>
    <h5>Tracking Security Metrics</h5>
    <Spacer />
    <AttackList :attacks="attacks" />
  </div>
</template>

<script>
import { ref } from 'vue';
import { AiProtocolsSquare } from '@kalimahapps/vue-icons/ai';
import AttackList from './components/AttackList.vue';
import Spacer from './components/Spacer.vue';
import attacks from './data/attacks.json';

export default {
  name: 'App',
  setup() {
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
html {
  height: 100%;
}

body {
  height: 100%;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.header {
  margin-top: 60px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.header > span {
  margin-right: 5px;
}
</style>
