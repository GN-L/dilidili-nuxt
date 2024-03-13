<template>
  <van-tabs v-model:active="active">
    <van-tab v-for="item in videoType" :key="item.id" :title="item.name">
      <h1>
        {{ item.name }}
      </h1>
    </van-tab>
  </van-tabs>
</template>

<script setup lang="ts">
const active = ref(0)
const { data: videoType } = await useFetch('/api/video_type')
</script>