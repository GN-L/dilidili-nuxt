<template>
  <div>
    <van-count-down :time="time" format="DD 天 HH 时 mm 分 ss 秒" />
    <div class="content">
      <div class="box">
        <NuxtLink to="/">
          <van-button type="primary">首页</van-button>
        </NuxtLink>
        <NuxtLink to="/video">
          <van-button type="success">视屏</van-button>
        </NuxtLink>
      </div>
      <div class="box">
        <NuxtPage />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
let time = ref(1000000000)
</script>

<style lang="scss">
/* :root{
  --van-primary-color: orange !important;
} */
.van-button--primary {
  background: orange !important;
  border: none !important;
  margin: 0 5px;
}
.content {
  display: flex;
  flex-direction: column;
  .box {
    margin: 10px 0 0 0;
  }
}
</style>