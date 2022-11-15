<template>
  <div class="attack-list-item">
    <div class="metric">
      <div class="metric-header">Attack Type:</div>
      <div class="metric-value">{{ attack.attack_type?.toUpperCase() }}</div>
    </div>
    <div class="metric">
      <div class="metric-header">Country</div>
      <div class="metric-value">{{ attack.country_code }}</div>
    </div>
    <div class="metric">
      <div class="metric-header">Threat Actor:</div>
      <div class="metric-value">{{ attack.threat_actor }}</div>
    </div>
    <div class="metric">
      <div class="metric-header">Asset Impact:</div>
      <div class="metric-value">{{ attack.asset_impact }}</div>
    </div>
    <div class="metric">
      <div class="metric-header">Clients Affected:</div>
      <div class="metric-value">
        {{ attack.clients_affected ? 'Yes' : 'No' }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AttackListing',
  props: {
    attack: Object,
  },
};
</script>

<style scoped>
.attack-list-item {
  display: flex;
  flex-direction: column;
  width: 100%;
  min-width: 100px;
  max-width: 500px;
  border-radius: 8px;
  margin: 24px 0;
  padding: 16px;
  font-size: 14px;
  background-color: #2c3e50;
}

.metric {
  color: white;
  margin: 6px 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.metric-header {
  font-weight: bold;
}
</style>
