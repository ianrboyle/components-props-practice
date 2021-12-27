<template>
  <div>
    <Child :child-message="parentMessage" />
    <!-- <Child /> -->
    <Sectors :sectors="sectors" />
  </div>
</template>

<script>
import Child from "@/components/Child.vue";
import axios from "axios";
import Sectors from "@/components/Sectors.vue";
export default {
  components: {
    Child,
    Sectors,
  },
  data: function () {
    return {
      parentMessage: "Herllo",
      sectors: [],
    };
  },
  created: function () {
    axios.get("http://localhost:3000/sectors").then((response) => {
      this.sectors = response.data;
      console.log(response.data);
    });
  },
};
</script>
