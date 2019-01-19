<template>
    <el-container direction="vertical">
      <div class="main">
            <div class="marvel-device macbook">
    <div class="top-bar"></div>
    <div class="camera"></div>
    <div class="screen">
        
    </div>
    <div class="bottom-bar"></div>
</div>
      </div>
    </el-container>
</template>
<script>

export default {
  data() {
    return {

    };
  },
  mounted(){
    
    
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
  .box-card {
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
  .box-card {
    margin: 20px;
    width: 100%;
    height: 100%;
  }
}
</style>

