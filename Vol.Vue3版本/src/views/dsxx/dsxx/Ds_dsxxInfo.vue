<template>
  <div class="dsxx">
    <VolForm
      ref="myform"
      :label-width="90"
      :loadKey="true"
      :formFields="formFields1"
      :formRules="formRules1"
    ></VolForm>
    <div style="text-align: center">
      <el-button type="primary" @click="submit">提交 </el-button>
    </div>
  </div>
</template>
<script>
import VolForm from "@/components/basic/VolForm.vue";
export default {
  components: { VolForm },
  methods: {
    submit() {
      this.$refs.myform.validate(() => {
        let formFields = JSON.parse(JSON.stringify(this.formFields1));
        formFields.HeadImageUrl = formFields.HeadImageUrl.map(c=>{return c.path}).join(",");

        let params={mainData:formFields};
          this.http
          .post("api/Ds_dsxx/updateInfo", params, true)
          .then((result) => {
             // this.$router.push({path:"/message"})
            this.$message.success("保存成功");
          });
        // this.http
        //   .post("api/Ds_dsxx/saveInfo", formFields, true)
        //   .then((result) => {
        //       this.$router.push({path:"/message"})
        //     this.$message.success("保存成功");
        //   });
      });
    },
  },
  data() {
    return {
      formFields1: {
        dsbh: "",
        dsxm: "",
        HeadImageUrl: [],
        xb: "",
        yxsh: "",
        csrq: "",
        yddh: "",
        dwdh: "",
        email: "",
        gzzwm: "",
        mzm: "",
        zzmmm: "",
        status: "",
        cszym: "",
        cszym1: "",
        cszym2: "",
        pzsdny: "",
        dslbm: "",
        whcdm: "",
        yjxkdm: "",
        zylydm: "",
        jbqk: "",
        yjfxqk: "",
        kyqk: "",
        hjqk: "",
        qtqk: "",
      },
      formRules1: [
        [{ title: "导师编号", required: true, field: "dsbh", disabled: true }],
        [{ title: "姓名", field: "dsxm", type: "text" }],

        [
          {
            dataKey: "gender",
            data: [],
            title: "性别",
            field: "xb",
            type: "select",
          },
        ],
        [
          {
            dataKey: "dic_yxs",
            data: [],
            title: "学院",
            field: "yxsh",
            type: "select",
          },
        ],
        //   [{"title":"出生日期","field":"csrq","type":"date"}],
        //   [{"title":"手机号","field":"yddh","type":"phone"}],
        //   [{"title":"单位电话","field":"dwdh"}],
        //   [{"title":"电子邮箱","field":"email"}],
        //   [{"dataKey":"dic_gbzw","data":[],"title":"行政职务码","field":"gzzwm","type":"select"}],
        //   [{"dataKey":"dic_mz","data":[],"title":"民族","field":"mzm","type":"select"}],
        //   [{"dataKey":"dic_zzmm","data":[],"title":"政治面貌","field":"zzmmm","type":"select"}],
        //   [{"title":"状态","field":"status"}],
        //   [{"dataKey":"现有专业","data":[],"title":"从事专业1","field":"cszym","type":"select"}],
        //   [{"dataKey":"现有专业","data":[],"title":"从事专业2","field":"cszym1","type":"select"}],
        //   [{"dataKey":"现有专业","data":[],"title":"从事专业3","field":"cszym2","type":"select"}],
        //   [{"title":"聘任硕导年月","field":"pzsdny"}],
        //   [{"title":"导师类别","field":"dslbm"}],
        //   [{"title":"最高学位学历","field":"whcdm"}],
        //   [{"dataKey":"dic_yjxk","data":[],"title":"一级学科","field":"yjxkdm","type":"select"}],
        //   [{"dataKey":"dic_zyly","data":[],"title":"专业领域","field":"zylydm","type":"select"}],
        //   [{"title":"基本情况","field":"jbqk","type":"editor"}],
        //   [{"title":"研究方向介绍","field":"yjfxqk","type":"editor"}],
        //   [{"title":"科研情况","field":"kyqk","type":"editor"}],
        //   [{"title":"获奖情况","field":"hjqk","type":"editor"}],
        [{ title: "头像", field: "HeadImageUrl", type: "img" ,  url: "/api/Ds_dsxx/Upload"}],
        [{ title: "其他情况", field: "qtqk", type: "editor" }],
      ],
    };
  },
  created() {
    this.http.get("api/Ds_dsxx/getInfo").then((result) => {
      this.formFields1 = result;
    });
  },
};
</script>
<style lang="less" scoped>
.dsxx {
  padding: 20px;
}
</style>