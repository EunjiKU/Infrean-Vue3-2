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
body {margin: 0; padding: 0; box-sizing: border-box;}
a {
  text-decoration: none;
  color: #34495e;
}
a:hover {
  color: #42b883;
}
a.router-link-exact-active {
  text-decoration: underline;
}

/* 트랜지션 효과 */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
