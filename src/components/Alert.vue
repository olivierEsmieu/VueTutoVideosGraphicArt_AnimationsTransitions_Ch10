<template>
  <div class="ui container">
    <transition name="bounce" appear mode="out-in">
      <div class="ui message success" v-if="toggle" key="visible">alert</div>
      <div class="ui message success" v-else key="invisible">else</div>
    </transition>
    <button class="ui button" @click="toggle = !toggle;">alert</button>
  </div>
</template>

<script>
export default {
  name: "Transitions",
  data: function() {
    return {
      toggle: true
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ui.container {
  margin-top: 10px;
}
/* v-enter-active (v-leave-active): délai + état final de l'élément  */
/* v-enter (v-leave) état au début de l'insertion (suppression) de l'élément */
/* rappel: chaque propriété CSS a une valeur par défaut. Ex: opacity: 1 */

.bounce-enter-active {
  animation: bounce-in 1s;
}
/*.bounce-leave-active {
  transition: opacity 1s;
  opacity: 0; 
}
*/

@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
</style>
