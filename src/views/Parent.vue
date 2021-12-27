<template>
  <div>
    <!-- <Child :child-message="parentMessage" /> -->
    <Child />
  </div>
</template>

<script>
import Child from "@/components/Child.vue";

export default {
  components: {
    Child,
  },
  data: function () {
    return {
      parentMessage: "",
    };
  },
};
</script>
