<template>
  <div>
    <h1>{{ childMessage }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    childMessage: { tpye: String, required: true, default: "Default String" },
  },
};
</script>
