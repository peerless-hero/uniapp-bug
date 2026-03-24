<!--
 * @Author: peerless_hero peerless_hero@outlook.com
 * @Date: 2024-09-28 02:40:32
 * @LastEditors: peerless_hero peerless_hero@outlook.com
 * @LastEditTime: 2026-03-24 22:24:05
 * @FilePath: \uniapp-bug\src\App.vue
 * @Description: 
 * 
-->
<script setup>
uni.onThemeChange(({ theme }) => {
  console.log('theme change, current is', theme)
})
</script>
