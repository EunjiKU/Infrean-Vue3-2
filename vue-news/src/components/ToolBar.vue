<template>
  <div class="header">
    <p>⭐섹션2(리팩토링1)⭐</p>||
    <router-link to="/news">News</router-link>||
    <router-link to="/ask">Ask</router-link>||
    <router-link to="/jobs">Jobs</router-link>||
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  padding: 8px;
  color: white;
  background-color: #42b883;
}
.header .router-link-exact-active {
  color: #35495e;
}
.header a {
  color: #fff;
}
</style>