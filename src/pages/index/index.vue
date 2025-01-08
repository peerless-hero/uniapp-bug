<!--
 * @Author: peerless_hero peerless_hero@outlook.com
 * @Date: 2024-09-28 02:40:32
 * @LastEditors: peerless_hero peerless_hero@outlook.com
 * @LastEditTime: 2025-01-08 20:25:33
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
    通过初始化蓝牙适配器触发索要蓝牙权限的弹窗
    <button type="primary" @click="openBluetoothAdapter">
      初始化蓝牙（openBluetoothAdapter）
    </button>
    <br />
    <button type="default" @click="getSystemSetting">获取设备设置（getSystemSetting）</button>
    <view>
      {{ systemSetting }}
    </view>
    <br />
    <button type="default" @click="getAppAuthorizeSetting">获取 APP 授权设置（getAppAuthorizeSetting）</button>
    <view>
      {{ authorizeSetting }}
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
      systemSetting: '',
      authorizeSetting: '',
    }
  },
  methods: {
    openBluetoothAdapter() {
      uni.openBluetoothAdapter()
    },
    getSystemSetting() {
      const setting = uni.getSystemSetting()
      this.systemSetting = JSON.stringify(setting)
    },
    getAppAuthorizeSetting() {
      const setting = uni.getAppAuthorizeSetting()
      this.authorizeSetting = JSON.stringify(setting)
    }
  }
}
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
}
</style>
