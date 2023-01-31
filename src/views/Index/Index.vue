<template>
    <div>
    <h3 style="margin-bottom:0px">
        用户总览
    </h3>
     <div style="">
      <el-row :gutter="20">
        <el-col :span="6">
          <div>
            <el-statistic group-separator="," :precision="2" :value="value2" :title="title"></el-statistic>
          </div>
        </el-col>
            <el-col :span="6">
          <div>
            <el-statistic  title="今日增长">
              <template slot="formatter">
                  456
              </template>

            </el-statistic>
          </div>
        </el-col>
        <el-col :span="6">
          <div>
            <el-statistic group-separator="," :precision="2" decimal-separator="." :value="value1" :title="title">
              <template slot="prefix">
                <i class="el-icon-s-flag" style="color: red"></i>
              </template>
              <template slot="suffix">
                <i class="el-icon-s-flag" style="color: blue"></i>
              </template>
            </el-statistic>
          </div>
    
    </el-col>
    <el-col :span="6">
      <div>
        <el-statistic :value="like ? 521 : 520" title="Feedback">
          <template slot="suffix">
            <span @click="like = !like" class="like">
              <i class="el-icon-star-on" style="color:red" v-show="!!like"></i>
              <i class="el-icon-star-off"  v-show="!like"></i>
            </span> </template>
        </el-statistic>
      </div>
    </el-col>
    </el-row>
  </div>
  <el-divider><i class="el-icon-mobile-phone"></i></el-divider>
</div>
</template>

<script>
export default {
    data() {
    return {
      like: true,
      value1: 4154.564,
      value2: 2222,
      title: "总用户数",
      input: "Hello Element UI!",
    };
  },
};


</script>

<style lang="less" scoped>
.like {
  cursor: pointer;
  font-size: 25px;
  display: inline-block;
}
</style>