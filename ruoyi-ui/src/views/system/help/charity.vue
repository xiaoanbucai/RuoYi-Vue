//家庭慈善救助页面 <
<template>
  <div class="app-container">
    <el-col :span="8">
      <el-card class="box-card1">
        <div slot="header" class="clearfix">
          <span style="text-align: center">家庭慈善救助办理常见问题以及办理指导</span>
        </div>
        <el-collapse v-model="activeNames" @change="handleChange">
          <el-collapse-item title="家庭慈善救助原则" name="1">
            <div>1.坚持“公开、公平、公正”的原则，接受社会各界监督；</div>
            <div>
              2.坚持“生活最困难、遭遇最不幸、社会最同情”的原则核定受助对象，救到急处、实处、难处；
            </div>
            <div>
              3.坚持“助困不助懒、扶贫更扶志”的原则，鼓励受助对象勤劳自救、积极进取，早日脱离困境；
            </div>
            <div>4.坚持以“慈善项目”为依托，针对符合项目条件的受助对象实施救助；</div>
            <div>
              5.坚持“不重复救助”的原则，对受助对象原则上每年度只救助一次，三年不超过两次救助，五年不超过三次救助。
            </div>
          </el-collapse-item>
          <el-collapse-item title="家庭慈善救助范围及对象" name="2">
            <div>
              1.具有郑州市户口，因患重大疾病或天灾人祸等突发事件导致生活困难者；因孤、老、残导致生活困难者。
            </div>
            <div>2.符合本会当年发布的慈善项目中的救助对象。</div>
            <div>3.根据捐赠者的意愿所实施的救助。</div>
            <div>4.根据上级要求，实施的省内外赈灾和援助项目。</div>
          </el-collapse-item>
          <el-collapse-item title="申请程序" name="3">
            <div>
              1.如符合当年郑州市慈善项目救助范围的，可以直接咨询项目合作单位、或直接到项目合作单位进行求助。
            </div>
            <div>
              2.如符合郑州慈善总会救急难项目救助范围的，可直接联系各县（市、区）、开发区慈善总会申请救助。
            </div>
            <div>
              3.如不符合当年郑州市慈善项目救助范围的，按照户籍属地管理的原则和谁募集谁使用的工作方针，各县（市）、区困难群众的临时救助由所在地慈善总会负责。
            </div>
            <div>
              4.向郑州慈善总会直接捐赠资金的单位干部、职工符合救助条件的，可由捐赠单位提出申请（提交材料与个人申请救助的材料相同），并填写《郑州慈善总会救助申请表》。
            </div>
            <div>
              5.捐赠者的定向救助，由定向捐赠协议中规定的救助对象提出申请及相关证明材料，并经捐赠方审核同意后，根据《郑州慈善总会章程》实施救助。
            </div>
          </el-collapse-item>
          <el-collapse-item title="所需提交材料:" name="5">
            <div>附申请人户口本和身份证复印件。</div>
            <div>属低保或低收入家庭的，需提供低保证或低收入家庭证明复印件；</div>
            <div>属残疾人的，需提供残疾人证复印件；</div>
            <div>
              属因病致贫的，应提供医疗单位的诊断证明、医疗费收据复印件，户口所在地县（区）、乡（街道办）、村（居）民委员会证明（需注明家庭成员基本信息）。
            </div>
          </el-collapse-item>
          <el-collapse-item title="各县（市）区慈善总会咨询电话:" name="6">
            <div>郑州慈善总会：68665328</div>
            <div>二七区：68769566</div>
            <div>管城区：66378793</div>
            <div>金水区：58579013</div>
            <div>中原区：67693811</div>
            <div>上街区：85701691</div>
            <div>经开区：66781811</div>
            <div>惠济区：63639736</div>
            <div>荥阳市：64650881</div>
            <div>新密市：69822497</div>
            <div>新郑市：69902200</div>
            <div>登封市：85506662</div>
            <div>中牟市：62188811</div>
            <div>高新区：67987922</div>
            <div>郑东新区：67179202</div>
            <div>航空港区：86199766</div>
          </el-collapse-item>
        </el-collapse>
      </el-card>
    </el-col>
    <el-col :span="8">
      <el-card class="box-card2">
        <div slot="header" class="clearfix">
          <span>业务办理相关材料提交</span>
        </div>
        <el-collapse v-model="activeNames" @change="handleChange"> </el-collapse>
        <el-upload
          style="text-align: center; margin-top: 20px"
          class="upload-demo"
          accept=".doc, .docx"
          action=""
          drag
          multiple
          :on-preview="handlePreview"
          :on-remove="handleRemove"
          :file-list="fileList"
          :on-exceed="handleExceed"
          :auto-upload="false"
        >
          <i class="el-icon-upload"></i>
          <div class="el-upload__text">将文件拖到此处，或<em>点击上传</em></div>
          <div class="el-upload__tip" slot="tip">
            <el-checkbox />是否更新已经存在的用户数据
            <el-link type="info" style="font-size: 12px" @click="importTemplate"
              >下载模板</el-link
            >
          </div>
        </el-upload>
      </el-card>
    </el-col>
  </div>
</template>

<script>
import { importTemplate } from "@/api/system/user";

export default {
  data() {
    return {
      activeNames: ["1"],
    };
  },
  methods: {
    submitUpload() {
      this.$refs.upload.submit();
    },
    handleRemove(file, fileList) {
      console.log(file, fileList);
    },
    handlePreview(file) {
      console.log(file);
    },
    handleChange(val) {
      console.log(val);
    },
    handleExceed(files, fileList) {
      this.$message.warning(
        `当前限制选择 3 个文件，本次选择了 ${files.length} 个文件，共选择了 ${
          files.length + fileList.length
        } 个文件`
      );
    },

    /** 下载模板操作 */
    importTemplate() {
      importTemplate().then((response) => {
        this.download(response.msg);
      });
    },
    // 文件上传中处理
    handleFileUploadProgress(event, file, fileList) {
      this.upload.isUploading = true;
    },
    // 文件上传成功处理
    handleFileSuccess(response, file, fileList) {
      this.upload.open = false;
      this.upload.isUploading = false;
      this.$refs.upload.clearFiles();
      this.$alert(response.msg, "导入结果", { dangerouslyUseHTMLString: true });
      this.getList();
    },
    // 提交上传文件
    submitFileForm() {
      this.$refs.upload.submit();
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

.box-card1 {
  width: 480px;
  margin-left: 48px;
}

.box-card2 {
  width: 480px;
  margin-left: 240px;
}
</style>
