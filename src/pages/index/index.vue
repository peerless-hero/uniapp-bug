<!--
 * @Author: peerless_hero peerless_hero@outlook.com
 * @Date: 2024-09-28 02:40:32
 * @LastEditors: peerless_hero peerless_hero@outlook.com
 * @LastEditTime: 2026-03-24 22:25:12
 * @FilePath: \uniapp-bug\src\pages\index\index.vue
 * @Description: 
 * 
-->
<template>
  <view class="content">
    <image class="logo" src="/static/logo.png"></image>
    <view class="text-area">
      <text class="title">{{ title }}</text>
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue'

const title = ref('Hello') 
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

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
  /* 此样式在HBuildX5.04深色模式下不生效 */
  @media (prefers-color-scheme: dark) {
    color: #ffffff;
  }
}
</style>
