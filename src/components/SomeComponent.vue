<template>
  <view class="text-area">
    <text class="title">{{ title }}</text>
  </view>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: ''
  }
}) 
</script>

<style>
.text-area {
  display: flex;
  justify-content: center;
}
</style>