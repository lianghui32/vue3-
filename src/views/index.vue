<template>
  <el-container class="layout">
    <el-header class="site-header">
      <my-header />
    </el-header>

    <el-main class="site-main">
      <my-main-content />
    </el-main>

    <el-footer class="site-footer">
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

.site-header {
  padding: 0;
  position: sticky;
  top: 0;
  z-index: 1000;
  backdrop-filter: blur(10px);
  /* background: rgba(255, 255, 255, 0.8); */
}

.site-main {
  flex: 1;
  padding: 0;
}

.site-footer {
  padding: 0;
}

@media (max-width: 768px) {
  .site-header {
    height: auto;
  }
}
</style>
