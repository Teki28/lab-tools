<template>
  <div>
    <el-header class="header">
      <el-col :span="6" class="title">
        <div class="grid-content bg-purple">Lab Tools</div>
      </el-col>
      <el-col :span="8">
        <div class="grid-content bg-purple btn1">
          <el-button round size="small" @click="routeDNA">
            DNA Quant
          </el-button>
        </div>
      </el-col>
      <el-col :span="5">
        <div class="grid-content bg-purple btn2">
          <el-button type="success" round size="small" @click="routeTool2">
            Tool2
          </el-button>
        </div>
      </el-col>
      <el-col :span="5">
        <div class="grid-content bg-purple btn3">
          <el-button type="primary" round size="small" @click="routeTool3">Tool3</el-button>
        </div>
      </el-col>
    </el-header>
    <nuxt />
  </div>
</template>

<script>
export default {
  methods: {
    routeDNA () {
      this.$router.push('/tool1')
    },
    routeTool2 () {
      window.location.href = "https://teki28.github.io/todo/"
    },
    routeTool3 () {
      this.$router.push('/tool3')
    }
  },
}
</script>

<style scoped>
.header {
  background-color: black;
}
.title {
  font-size: 4vw;
  color: whitesmoke;
  line-height: 60px;
}
.btn1,
.btn2,
.btn3 {
  margin-top: 12px;
}
</style>