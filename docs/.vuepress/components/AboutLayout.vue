<template>
    <el-container direction="vertical">
      <div class="main">
            <el-card class="box-card">
              <h1 align="center">关于我</h1>
              <p>
                
              </p>

            </el-card>
      </div>
    </el-container>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {
    
  }
};
</script>
<style scoped>
@media (min-width: 1201px) {
  .main {
    padding-top: 50px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .box-card{
    margin: 20px;
    width: 100%;
    height: 100%;
  }
}

@media (max-width: 1020px) {
  .main {
    padding-top: 20px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .box-card{
    margin: 20px;
    width: 100%;
    height: 100%;
  }
}
</style>

