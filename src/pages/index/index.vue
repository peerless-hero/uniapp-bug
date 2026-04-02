<template>
  <view class="content">
    <image class="logo" src="/static/logo.png"></image>
    <some-component v-bind="data" />
  </view>
</template>

<script setup>
import SomeComponent from '@/components/SomeComponent.vue'

const data = reactive({
  // prop属性
  title: 'Hello',
})
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
