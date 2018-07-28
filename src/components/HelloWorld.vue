<template>
  <b-container fluid id="main-container">
    <b-row class="text-center">

      <b-col sm="12" lg="5">
        <about-summary/>
      </b-col>

      <b-col cols="1" offset="1">
        <b-form-group label="Example Filters">
          <b-form-checkbox-group stacked v-model="selected" name="flavour2" :options="options" />
        </b-form-group>
      </b-col>

      <b-col sm="10" lg="4">
        <map-card/>
      </b-col>

    </b-row>
  </b-container>
</template>

<script>
import AboutSummary from "./AboutSummary"
import MapCard from "./MapCard"
export default {
  name: 'HelloWorld',
  components: {
    AboutSummary,
    MapCard
  },
  props: {
    msg: String
  },
  data () {
    return {
      selected: [], // Must be an array reference!
      options: [
        {text: 'Filter 1', value: 'orange'},
        {text: 'Filter 2', value: 'apple'},
        {text: 'Filter 3', value: 'pineapple'},
        {text: 'Filter 4', value: 'grape'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  #main-container {
    padding-top: 8vh;
  }


// h3 {
//   margin: 40px 0 0;
// }
// ul {
//   list-style-type: none;
//   padding: 0;
// }
// li {
//   display: inline-block;
//   margin: 0 10px;
// }
// a {
//   color: #42b983;
// }
</style>
