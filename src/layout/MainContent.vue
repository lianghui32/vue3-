<template>
  <div class="main-content">
    <el-row :gutter="20">
      <el-col :span="8">
        <el-card class="glass-card" shadow="hover">
          <template v-slot:header>
            <div>项目展示</div>
          </template>
          <!-- 项目内容 -->
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="glass-card" shadow="hover">
          <template v-slot:header>
            <div>技能介绍</div>
          </template>
          <!-- 技能内容 -->
        </el-card>
      </el-col>
      <el-col :span="8">
        <el-card class="glass-card" shadow="hover">
          <template v-slot:header>
            <div>工作经历</div>
          </template>
          <!-- 经历内容 -->
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
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
