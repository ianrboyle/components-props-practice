<template>
  <div><Child :message="'Hello'" /></div>
</template>

<script>
import Child from "@/components/Child.vue";

export default {
  components: {
    Child,
  },
  data: function () {
    return {
      text: "",
      message: "",
    };
  },
};
</script>
