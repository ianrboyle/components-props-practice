<template>
  <div>
    <Child :child-message="parentMessage" />
    <!-- <Child /> -->
    <Sectors :sectors="sectors" />
    <Industries />
  </div>
</template>

<script>
import Child from "@/components/Child.vue";
import axios from "axios";
import Sectors from "@/components/Sectors.vue";
import Industries from "@/components/Industries.vue";
export default {
  components: {
    Child,
    Sectors,
    Industries,
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
