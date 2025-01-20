<!--
 * @Author: zhaojinfeng 121016171@qq.com
 * @Date: 2025-01-20 14:58:17
 * @LastEditors: zhaojinfeng 121016171@qq.com
 * @LastEditTime: 2025-01-20 15:24:27
 * @FilePath: \uniapp-bug\src\pages\index\index.vue
 * @Description: 
 * 
-->
<template>
  <view class="content">
    <image class="logo" src="/static/logo.png"></image>
    <button type="primary" @click="upload">上传</button>
  </view>
</template>

<script>
function createUpload(path) {
  console.log('start', path);
  
  const task = plus.uploader.createUpload("https://apifoxmock.com/m1/5737516-5420210-default/status/200",
    { method: "POST", timeout: 2 },
    function (t, status) { 
      // 上传完成
      if (status == 200) {
        console.log("Upload success: " + t.url);
      } else {
        console.log("Upload failed: " + status);
      }
    }
  );
  task.addFile(path, { key: 'file' });
  // 此为自定义mock 超时参数
  task.addData("timeout", "11");
  task.start();
}

export default {
  methods: {
    upload() {
      uni.chooseImage({
        count: 1,
        success: (res) => {
          createUpload(res.tempFilePaths[0])
        }
      })
    }
  },
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
</style>
