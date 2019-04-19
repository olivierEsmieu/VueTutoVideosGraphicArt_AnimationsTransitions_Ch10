<template>
  <div class="ui main container">
    <div id="app" class="ui inverted menu">
      <a class="item" @click="show = 'alert';">Alert</a>
      <a class="item" @click="show = 'transition';">Transitions</a>
      <a class="item" @click="show = 'list';">List</a>
    </div>
    <!-- transition (sans s: reservé vue) -->
    <alert v-if="show == 'alert'" />
    <transitions v-if="show == 'transition'" />
    <list v-if="show == 'list'" />
  </div>
</template>

<script>
import Alert from "./components/Alert";
import Transitions from "./components/Transitions";
import List from "./components/List";

export default {
  name: "App",
  components: {
    Alert,
    Transitions,
    List
  },
  data: function() {
    return {
      show: "alert"
    };
  }
};
</script>

<style>
/*
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
//  -webkit-font-smoothing: antialiased;
//  -moz-osx-font-smoothing: grayscale;
  //text-align: center;
 // color: #2c3e50;
 // margin-top: 20px;
}
*/
</style>
