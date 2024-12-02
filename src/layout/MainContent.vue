<template>
  <div class="main-content">
    <el-row :gutter="20">
      <el-col v-for="card in cards" :key="card.title" :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
        <el-card class="glass-card" shadow="hover">
          <template #header>
            <div class="card-header">
              {{ card.title }}
            </div>
          </template>
          {{ card.content }}
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script setup>
const cards = [
  { title: '项目展示', content: '项目内容' },
  { title: '技能介绍', content: '技能内容' },
  { title: '工作经历', content: '经历内容' },
]
</script>

<style scoped>
.main-content {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.glass-card {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(10px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.3);
  margin-bottom: 20px;
  height: 100%;
}

.card-header {
  font-weight: bold;
}

@media (max-width: 768px) {
  .main-content {
    padding: 10px;
  }
}
</style>
