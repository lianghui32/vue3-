<template>
  <el-container class="layout">
    <el-header>
      <my-header />
    </el-header>

    <el-main>
      <my-main-content />
    </el-main>

    <el-footer>
      <my-footer />
    </el-footer>
  </el-container>
</template>

<script setup>
import MyHeader from '@/layout/Header.vue'
import MyMainContent from '@/layout/MainContent.vue'
import MyFooter from '@/layout/Footer.vue'
</script>

<style scoped>
.layout {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.el-header,
.el-footer {
  padding: 0;
}

.el-main {
  flex: 1;
}

.main-content {
  padding: 50px;
}

.glass-card {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(10px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.3);
}
</style>
