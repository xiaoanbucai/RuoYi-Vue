<template>
  <div class="dashboard-editor-container">
    <div class="block">
      <el-carousel height="550px" interval="5000">
        <el-carousel-item>
          <div>
            <el-row style="background: #fff; padding: 5% 64px 5% 64px">
              <PanelGroup />
            </el-row>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div>
            <el-row style="background: #fff; padding: 5% 64px 5% 64px">
              <line-chart />
            </el-row>
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div>
          
          </div>
        </el-carousel-item>

        <el-carousel-item>
          <div>

          
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
import PanelGroup from "./dashboard/PanelGroup";
import LineChart from "./dashboard/LineChart";

export default {
  name: "Index",
  components: {
    LineChart,
    PanelGroup,
  },
};
</script>

<style lang="scss" scoped>
.dashboard-editor-container {
  padding: 32px;
  background-color: rgb(240, 242, 245);
  position: relative;

  .chart-wrapper {
    background: #fff;
    padding: 16px 16px 0;
    margin-bottom: 32px;
  }
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

@media (max-width: 1024px) {
  .chart-wrapper {
    padding: 8px;
  }
}
</style>
