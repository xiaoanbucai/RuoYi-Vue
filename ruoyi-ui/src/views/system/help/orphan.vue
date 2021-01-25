//孤儿救助金办理页面
<template>
  <div class="app-container">
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>孤儿救助金办理常见问题以及办理指导</span>
        <!-- <el-button style="float: right; padding: 3px 0" type="text">上传文件</el-button> -->
      </div>
      <el-collapse v-model="activeNames" @change="handleChange">
        <el-collapse-item title="郑州低保标准" name="1">
          <div>城镇低保标准</div>
          <div>
            从2015年7月1日起，郑州市城市低保标准将由现在每人每月470元提高至520元。
          </div>
          <div>农村低保标准</div>
          <div>从2015年7月1日起，郑州市农村低保标准由每人每月260元提高至290元。</div>
        </el-collapse-item>
      </el-collapse>
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeNames: ["1"],
    };
  },
  methods: {
    handleChange(val) {
      console.log(val);
    },
  },
};
</script>

<style>
.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

.box-card {
  width: 480px;
}
</style>
