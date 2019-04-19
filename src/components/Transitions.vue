<template>
  <div class="ui container">
    <button class="ui left floated button" @click="show = !show;">
      affiche
    </button>
    <transition name="fade">
      <h2 class="ui header" v-if="show">ehehe</h2>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Transitions",
  data: function() {
    return {
      show: true
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ui.container {
  margin-top: 10px;
}
.fade-enter-active, /* transition d'entrée: délai fade-enter =>fade-enter-to */
.fade-leave-active {
  /* transition de sortie: délai pour fade-leave =>fade-leave-to */
  transition: opacity 2s;
}
.fade-enter /* Résultat quand la transaction entre */ {
  opacity: 0.1;
}
.fade-enter-to /* Résultat quand la transaction  est entrée */ {
  opacity: 1;
}
.fade-leave/* Résultat qund la transition sort */ {
  opacity: 1;
}
.fade-leave-to /* Résultat quand la transition est sortiec */ {
  opacity: 0.5;
}
</style>
