<template>
  <div class="header">
    <div class="logo">Lianghui</div>
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal">
      <el-menu-item index="1">首页</el-menu-item>
      <el-menu-item index="2">项目</el-menu-item>
      <el-menu-item index="3">关于我</el-menu-item>
      <el-menu-item index="4">联系方式</el-menu-item>
    </el-menu>
    <div class="social-icons">
      <div
        v-for="(icon, index) in socialIcons"
        :key="index"
        class="social-icon"
        @click="openLink(icon.link)"
        :title="icon.name"
      >
        <img :src="icon.image" :alt="icon.name" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import github from '@/assets/img/github.png'
import gitee from '@/assets/img/Gitee.png'
import CSDN from '@/assets/img/CSDN.png'
import newcoder from '@/assets/img/newcoder.png'
const activeIndex = ref('1')

const socialIcons = ref([
  {
    name: 'GitHub',
    link: 'https://github.com/lianghui32?tab=repositories',
    image: github,
  },
  {
    name: 'Gitee',
    link: 'https://gitee.com/lianghui2333',
    image: gitee,
  },
  {
    name: 'CSDN',
    link: 'https://blog.csdn.net/qq_52313022',
    image: CSDN,
  },
  {
    name: 'newcoder',
    link: 'https://www.nowcoder.com/users/925753281',
    image: newcoder,
  },
  // 可以添加更多社交图标
])

function openLink(url) {
  window.open(url, '_blank')
}
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* background: #fff; */
  padding: 0 50px;
}

.logo {
  font-size: 20px;
  font-weight: bold;
}

.el-menu-demo {
  background: transparent;
}
.el-menu-item {
  font-size: 16px;
  color: #000000;
}
.social-icons {
  display: flex;
  gap: 10px;
}

.social-icon {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  cursor: pointer;
  transition: transform 0.2s;
}

.social-icon:hover {
  transform: scale(1.1);
}

.social-icon img {
  width: 100%;
  height: 100%;
}
</style>
