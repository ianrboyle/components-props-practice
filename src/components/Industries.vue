<template>
  <div><IndustryIndex :industries="industries" /></div>
</template>

<script>
import axios from "axios";
import IndustryIndex from "@/components/IndustryIndex";
export default {
  components: {
    IndustryIndex,
  },
  data: function () {
    return {
      industries: [],
    };
  },
  created: function () {
    axios.get("http://localhost:3000/industries").then((response) => {
      this.industries = response.data;
      console.log(response.data);
    });
  },
};
</script>
