//孤儿救助金办理页面
<template>
  <div class="app-container">
    <el-col :span="8">
      <el-card class="box-card">
        <div slot="header" class="clearfix">
          <span>孤儿救助金办理常见问题以及办理指导</span>
          <!-- <el-button style="float: right; padding: 3px 0" type="text">上传文件</el-button> -->
        </div>
        <el-collapse v-model="activeNames" @change="handleChange">
          <el-collapse-item title="散居孤儿申请孤儿基本生活费条件以及所需材料" name="1">
            <div>
              由孤儿监护人（抚养人）向孤儿户籍所在地街道办事处或乡（镇）人民政府提出申请。
            </div>
            <div>申请时应提交以下材料：</div>
            <div>
              1.公安机关出具的孤儿父母死亡户口本销户页或证明，或医院出具的孤儿父母死亡证明，或殡仪馆出具的孤儿父母死亡火化证明，或人民法院出具的孤儿父母宣告死亡或失踪的证明法律文书原件;
            </div>
            <div>2.孤儿身份证（或户口本）原件；</div>
            <div>3.孤儿监护人（抚养人）身份证（或户口本）原件；</div>
            <div>4.孤儿近期1寸免冠照片2张；</div>
            <div>5.孤儿监护人（抚养人）的贫困证明；</div>
            <div>6.残疾孤儿需提供残疾证明。</div>
          </el-collapse-item>
          <el-collapse-item title="散居孤儿申请孤儿基本生活费审核流程" name="2">
            <div>
              街道办事处或乡（镇）人民政府应在10个工作日内，组织有关人员通过入户调查、邻里访问等方式，对监护人（抚养人）和社会散居孤儿情况进行认真核实。
            </div>
            <div>
              符合认定条件的，由孤儿本人或监护人（抚养人）填写《孤儿基本生活费申报审批表》一式两份，街道办事处或乡（镇）人民政府签署审查意见后，连同有关证明材料的复印件一并报县级民政部门审批。
            </div>
          </el-collapse-item>
          <el-collapse-item title="散居孤儿申请孤儿基本生活费审批流程" name="3">
            <div>
              县级民政部门要认真审核申请材料，符合条件的，应在10个工作日内作出审批决定，并将审批结果函告街道办事处或乡（镇）人民政府。
            </div>
            <div>
              县级民政部门应同时与社会散居孤儿的监护人（抚养人）签定孤儿养育协议，对领取、使用孤儿基本生活费以及孤儿养育状况提出相应要求，明确监护人（抚养人）应依法履行的监护职责和抚养义务。
            </div>
            <div>签订孤儿养育协议应征求和尊重孤儿本人意愿。</div>
            <div>孤儿监护人（抚养人）发生变化的，应按照以上程序重新办理有关手续。</div>
          </el-collapse-item>
          <el-collapse-item title="如何办理孤儿证：" name="4">
            <div>孤儿是指失去父母的儿童。</div>
            <div>
              凡具有本地户口、年龄未满十八周岁,失去父母,经户口所在地县民政部门审核,报市民政局认定批准后发给《孤儿证》的儿童。
            </div>
          </el-collapse-item>
          <el-collapse-item title="办理孤儿证申请材料：" name="5">
            <div>1、户口簿(父母死亡户籍证明)；</div>
            <div>2、生父母死亡或者宣告死亡的证明。</div>
            <div>
              孤儿的父母因病自然死亡的，凡死于医疗机构的，死亡证明由该医疗机构出具；死于家中的，死亡证明由负责该地区的基层医疗卫生组织出具；
            </div>
            <div>
              凡非正常死亡或不能确定是否属于正常死亡者，需经公安部门判定性质并出具死亡证明；宣告死亡的证明则应由人民法院出具。
            </div>
          </el-collapse-item>
          <el-collapse-item title="办理孤儿证办理程序：" name="6">
            <div>1.由本人提出书面申请并附户口簿复印件</div>
            <div>2.村委会调查落实</div>
            <div>3.乡民政办核实并填报审批表</div>
            <div>4.交分管领导签字审批</div>
            <div>5.报县民政局审批</div>
            <div>6.由县民政局填报孤儿证</div>
            <div>7.转乡民政办审批并通知申请人领取孤儿证</div>
          </el-collapse-item>
        </el-collapse>
      </el-card>
    </el-col>
    <el-col :span="8">
      <el-card class="box-card2">
        <div slot="header" class="clearfix">
          <span>业务办理相关材料提交</span>
        </div>
      </el-card>
    </el-col>
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

.box-card2 {
  width: 480px;
  margin-left: 240px;
}
</style>
