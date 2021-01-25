<template>
  <el-row :gutter="40" class="panel-group">
    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-people">
            <svg-icon icon-class="peoples" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">代办业务</div>
          </div>
        </el-link>
      </div>
    </el-col>
    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-message">
            <svg-icon icon-class="button" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">帮扶业务</div>
          </div>
        </el-link>
      </div>
    </el-col>
    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-money">
            <svg-icon icon-class="chart" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">社区业务</div>
          </div>
        </el-link>
      </div>
    </el-col>
    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-shopping">
            <svg-icon icon-class="star" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">党团志愿</div>
          </div>
        </el-link>
      </div>
    </el-col>

    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-education">
            <svg-icon icon-class="table" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">宣传服务</div>
          </div>
        </el-link>
      </div>
    </el-col>
    <el-col :xs="8" :sm="8" :lg="8" class="card-panel-col">
      <div class="card-panel">
        <el-link
          :underline="false"
          href="https://element.eleme.io"
          style="width: 248px; height: 128px"
        >
          <div class="card-panel-icon-wrapper icon-education">
            <svg-icon icon-class="question" class-name="card-panel-icon" />
          </div>
          <div class="card-panel-description">
            <div class="card-panel-text" style="margin-left: 30px">问题咨询</div>
          </div>
        </el-link>
      </div>
    </el-col>
  </el-row>
</template>

<style lang="scss" scoped>
.panel-group {
  margin-top: 36px;

  .card-panel-col {
    margin-bottom: 32px;
  }

  .card-panel {
    height: 128px;
    cursor: pointer;
    font-size: 22px;
    position: relative;
    overflow: hidden;
    color: #666;
    background: #fff;
    box-shadow: 4px 4px 40px rgba(0, 0, 0, 0.05);
    border-color: rgba(0, 0, 0, 0.05);
    margin: 10% 5% 5% 10%;

    &:hover {
      .card-panel-icon-wrapper {
        color: #fff;
      }

      .icon-people {
        background: #40c9c6;
      }

      .icon-message {
        background: #36a3f7;
      }

      .icon-money {
        background: #f4516c;
      }

      .icon-shopping {
        background: #34bfa3;
      }

      .icon-education {
        background: #34bfa3;
      }
    }

    .icon-people {
      color: #40c9c6;
    }

    .icon-message {
      color: #36a3f7;
    }

    .icon-money {
      color: #f4516c;
    }

    .icon-shopping {
      color: #34bfa3;
    }

    .icon-education {
      color: #34bfa3;
    }

    .card-panel-icon-wrapper {
      float: left;
      margin: 14px 0 0 14px;
      padding: 16px;
      transition: all 0.38s ease-out;
      border-radius: 6px;
    }

    .card-panel-icon {
      float: left;
      font-size: 48px;
    }

    .card-panel-description {
      float: right;
      font-weight: bold;
      margin: 30px;
      margin-left: 0px;
      position: center;

      .card-panel-text {
        line-height: 22px;
        color: rgba(0, 0, 0, 0.45);
        font-size: 20px;

        margin-bottom: 14px;
      }

      .card-panel-num {
        font-size: 20px;
      }
    }
  }
}

@media (max-width: 550px) {
  .card-panel-description {
    display: none;
  }

  .card-panel-icon-wrapper {
    float: none !important;
    width: 100%;
    height: 100%;
    margin: 0 !important;

    .svg-icon {
      display: block;
      margin: 14px auto !important;
      float: none !important;
    }
  }
}
</style>
