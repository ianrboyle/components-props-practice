<template>
  <div>
    <div v-for="sector in sectors" :key="sector.id">{{ sector.sector }}</div>
  </div>
</template>

<script>
export default {
  props: {
    sectors: { tpye: Array },
  },
};
</script>
