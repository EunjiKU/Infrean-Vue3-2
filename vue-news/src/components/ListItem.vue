<template>
  <ul class="news-list">
    <li v-for="item in  this.$store.state.news" v-bind:key="item" class="post">
      <!-- 포인트 영역 -->
      <div class="points">
        {{ item.points }}
      </div>
      <!-- 기타 정보 영역 -->
      <div>
        <p class="news-title">
          <a v-bind:href="item.url">
          {{ item.title }}
          </a>
        </p>
        <small class="link-text">
          {{ item.time_ago }} by
          <router-link v-bind:to="`/user/${item.user}`" class="link-text">{{ item.user }}</router-link>
        </small>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  created() {
    this.$store.dispatch('FETCH_NEWS');
  }
}
</script>

<style>
  .news-list {
    margin: 0;
    padding: 0;
  }
  .post {
    display: flex;
    align-content: center;
    list-style: none;
    border-bottom: 1px solid #ddd;
  }
  .points {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 80px;
    height: 60px;
    color: #42b883
  }
  .news-title {
    margin: 0;
  }
  .link-text {
    color: #828282;
  }
</style>