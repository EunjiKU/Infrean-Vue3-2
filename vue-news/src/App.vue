<template>
  <div id="app">
    <tool-bar></tool-bar>
    <Transition name="fade">
    <router-view></router-view>
    </Transition>
  </div>
</template>

<script>
import ToolBar from './components/ToolBar.vue'

export default {
  name: "App",
  components: {
    ToolBar
  }
};
</script>
<style>
* {margin: 0; padding: 0; box-sizing: border-box;}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
