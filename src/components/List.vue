<template>
  <div class="ui main container">
    <ul>
      <transition-group name="bounce" tag="ul">
        <li v-for="item in items" :key="item">{{ item }}</li>
      </transition-group>
    </ul>
    <button class="ui button" @click="add">add</button>
  </div>
</template>

<script>
export default {
  name: "Lists",
  data: function() {
    return {
      items: [1, 2, 3, 4]
    };
  },
  methods: {
    add: function() {
      this.items.push(Math.random());
    }
  }
};
</script>
<style scoped>
.ui.main.container {
  margin-top: 20px;
}
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
</style>
