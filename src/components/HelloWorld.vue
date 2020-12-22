<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
import _ from "lodash";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  mounted() {
    console.info("paper mounted");
    const data = {
      dims: [
        "AI Guide_Base",
        "AI Guide_Simul.",
        "D/C Rate_Base",
        "D/C Rate_Simul."
      ],
      weeks: 52
    };

    const result = _.chain(data.dims)
      .map(r => {
        return { dim: r };
      })
      .value();
    console.log("###");
    console.log(result);
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
