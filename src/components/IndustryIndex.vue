<template>
  <div>
    <div v-for="industry in industries" :key="industry.id">{{ industry.industry }}</div>
  </div>
</template>

<script>
export default {
  props: {
    industries: { tpye: Array },
  },
};
</script>
