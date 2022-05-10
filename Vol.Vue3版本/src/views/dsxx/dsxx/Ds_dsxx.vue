<!--
*Author：jxx
 *Contact：283591387@qq.com
 *代码由框架生成,任何更改都可能导致被代码生成器覆盖
 *业务请在@/extension/system/dsxx/Ds_dsxx.js此处编写
 -->
<template>
    <view-grid ref="grid"
               :columns="columns"
               :detail="detail"
               :editFormFields="editFormFields"
               :editFormOptions="editFormOptions"
               :searchFormFields="searchFormFields"
               :searchFormOptions="searchFormOptions"
               :table="table"
               :extend="extend">
    </view-grid>
</template>
<script>
    import extend from "@/extension/dsxx/dsxx/Ds_dsxx.js";
    import { ref, defineComponent } from "vue";
    export default defineComponent({
        setup() {
            const table = ref({
                key: 'id',
                footer: "Foots",
                cnName: '导师信息',
                name: 'dsxx/Ds_dsxx',
                url: "/Ds_dsxx/",
                sortName: "dsbh"
            });
            const editFormFields = ref({"dsbh":"","dsxm":"","HeadImageUrl":"","xb":"","yxsh":"","csrq":"","yddh":"","dwdh":"","email":"","gzzwm":"","mzm":"","zzmmm":"","status":"","cszym":"","cszym1":"","cszym2":"","pzsdny":"","dslbm":"","whcdm":"","yjxkdm":"","zylydm":"","jbqk":"","yjfxqk":"","kyqk":"","hjqk":"","qtqk":""});
            const editFormOptions = ref([[{"title":"导师编号","required":true,"field":"dsbh","disabled":true}],
                              [{"title":"姓名","field":"dsxm","type":"text"}],
                              [{"title":"头像","field":"HeadImageUrl","type":"img"}],
                              [{"dataKey":"gender","data":[],"title":"性别","field":"xb","type":"select"}],
                              [{"dataKey":"dic_yxs","data":[],"title":"学院","field":"yxsh","type":"select"}],
                              [{"title":"出生日期","field":"csrq","type":"date"}],
                              [{"title":"手机号","field":"yddh","type":"phone"}],
                              [{"title":"单位电话","field":"dwdh"}],
                              [{"title":"电子邮箱","field":"email"}],
                              [{"dataKey":"dic_gbzw","data":[],"title":"行政职务码","field":"gzzwm","type":"select"}],
                              [{"dataKey":"dic_mz","data":[],"title":"民族","field":"mzm","type":"select"}],
                              [{"dataKey":"dic_zzmm","data":[],"title":"政治面貌","field":"zzmmm","type":"select"}],
                              [{"title":"状态","field":"status"}],
                              [{"dataKey":"现有专业","data":[],"title":"从事专业1","field":"cszym","type":"select"}],
                              [{"dataKey":"现有专业","data":[],"title":"从事专业2","field":"cszym1","type":"select"}],
                              [{"dataKey":"现有专业","data":[],"title":"从事专业3","field":"cszym2","type":"select"}],
                              [{"title":"聘任硕导年月","field":"pzsdny"}],
                              [{"title":"导师类别","field":"dslbm"}],
                              [{"title":"最高学位学历","field":"whcdm"}],
                              [{"dataKey":"dic_yjxk","data":[],"title":"一级学科","field":"yjxkdm","type":"select"}],
                              [{"dataKey":"dic_zyly","data":[],"title":"专业领域","field":"zylydm","type":"select"}],
                              [{"title":"基本情况","field":"jbqk","type":"editor"}],
                              [{"title":"研究方向介绍","field":"yjfxqk","type":"editor"}],
                              [{"title":"科研情况","field":"kyqk","type":"editor"}],
                              [{"title":"获奖情况","field":"hjqk","type":"editor"}],
                              [{"title":"其他情况","field":"qtqk","type":"editor"}]]);
            const searchFormFields = ref({});
            const searchFormOptions = ref([]);
            const columns = ref([{field:'id',title:'id',type:'long',width:110,hidden:true,readonly:true,require:true,align:'left'},
                       {field:'User_Id',title:'User_Id',type:'int',width:110,hidden:true,align:'left'},
                       {field:'dsbh',title:'导师编号',type:'string',sort:true,width:110,readonly:true,require:true,align:'left',sort:true},
                       {field:'passwd',title:'passwd',type:'string',width:110,hidden:true,align:'left'},
                       {field:'dsxm',title:'姓名',type:'string',sort:true,width:110,align:'left'},
                       {field:'HeadImageUrl',title:'头像',type:'img',width:180,align:'left'},
                       {field:'xb',title:'性别',type:'string',bind:{ key:'gender',data:[]},width:110,align:'left'},
                       {field:'yxsh',title:'学院',type:'string',bind:{ key:'dic_yxs',data:[]},width:110,align:'left'},
                       {field:'sfz',title:'身份证号',type:'string',width:110,align:'left'},
                       {field:'yddh',title:'手机号',type:'string',width:110,hidden:true,align:'left'},
                       {field:'dwdh',title:'单位电话',type:'string',width:110,hidden:true,align:'left'},
                       {field:'zzdh',title:'住宅电话',type:'string',width:110,hidden:true,align:'left'},
                       {field:'gzzwm',title:'行政职务码',type:'string',bind:{ key:'dic_gbzw',data:[]},width:110,align:'left'},
                       {field:'csrq',title:'出生日期',type:'date',width:110,align:'left'},
                       {field:'jszcm',title:'职称',type:'string',width:110,hidden:true,align:'left'},
                       {field:'mzm',title:'民族',type:'string',bind:{ key:'dic_mz',data:[]},width:110,hidden:true,align:'left'},
                       {field:'zzmmm',title:'政治面貌',type:'string',bind:{ key:'dic_zzmm',data:[]},width:110,hidden:true,align:'left'},
                       {field:'status',title:'状态',type:'string',width:110,align:'left'},
                       {field:'role',title:'角色',type:'string',width:110,hidden:true,align:'left'},
                       {field:'cszym',title:'从事专业1',type:'string',bind:{ key:'现有专业',data:[]},width:110,hidden:true,align:'left'},
                       {field:'cszym1',title:'从事专业2',type:'string',bind:{ key:'现有专业',data:[]},width:110,hidden:true,align:'left'},
                       {field:'cszym2',title:'从事专业3',type:'string',bind:{ key:'现有专业',data:[]},width:110,hidden:true,align:'left'},
                       {field:'pzsdny',title:'聘任硕导年月',type:'string',width:110,hidden:true,align:'left'},
                       {field:'pzbdny',title:'聘任博导年月',type:'string',width:110,hidden:true,align:'left'},
                       {field:'dslbm',title:'导师类别',type:'string',width:110,align:'left'},
                       {field:'whcdm',title:'最高学位学历',type:'string',width:110,align:'left'},
                       {field:'hxwyx',title:'获学位学校',type:'string',width:110,hidden:true,align:'left'},
                       {field:'hxwsj',title:'获学位时间',type:'string',width:110,hidden:true,align:'left'},
                       {field:'hxlyx',title:'获学历学校',type:'string',width:110,hidden:true,align:'left'},
                       {field:'hxlsj',title:'获学历日期',type:'string',width:110,hidden:true,align:'left'},
                       {field:'yjxkdm',title:'一级学科',type:'string',bind:{ key:'dic_yjxk',data:[]},width:110,align:'left'},
                       {field:'zylydm',title:'专业领域',type:'string',bind:{ key:'dic_zyly',data:[]},width:110,align:'left'},
                       {field:'zydm',title:'专业代码',type:'string',width:110,hidden:true,align:'left'},
                       {field:'yjfx',title:'研究方向',type:'string',width:120,hidden:true,align:'left'},
                       {field:'dsjl',title:'导师简历',type:'string',width:110,hidden:true,align:'left'},
                       {field:'bz',title:'备注',type:'string',width:110,hidden:true,align:'left'},
                       {field:'jbqk',title:'基本情况',type:'string',width:110,hidden:true,align:'left'},
                       {field:'yjfxqk',title:'研究方向介绍',type:'string',width:110,hidden:true,align:'left'},
                       {field:'kyqk',title:'科研情况',type:'string',width:110,hidden:true,align:'left'},
                       {field:'hjqk',title:'获奖情况',type:'string',width:110,hidden:true,align:'left'},
                       {field:'qtqk',title:'其他情况',type:'string',width:110,hidden:true,align:'left'},
                       {field:'CreateDate',title:'CreateDate',type:'datetime',width:110,hidden:true,align:'left',sort:true},
                       {field:'CreateID',title:'CreateID',type:'int',width:80,hidden:true,align:'left'},
                       {field:'Creator',title:'Creator',type:'string',width:130,hidden:true,align:'left'},
                       {field:'Modifier',title:'Modifier',type:'string',width:130,hidden:true,align:'left'},
                       {field:'ModifyDate',title:'ModifyDate',type:'datetime',width:110,hidden:true,align:'left',sort:true},
                       {field:'ModifyID',title:'ModifyID',type:'int',width:80,hidden:true,align:'left'},
                       {field:'AuditDate',title:'AuditDate',type:'datetime',width:110,hidden:true,align:'left',sort:true},
                       {field:'AuditStatus',title:'审核状态',type:'int',width:110,align:'left'},
                       {field:'Auditor',title:'Auditor',type:'string',width:180,hidden:true,align:'left'},
                       {field:'Auditreason',title:'Auditreason',type:'string',width:180,hidden:true,align:'left'},
                       {field:'AuditId',title:'AuditId',type:'int',width:110,hidden:true,align:'left'},
                       {field:'email',title:'电子邮箱',type:'string',width:110,align:'left'}]);
            const detail = ref({
                cnName: "#detailCnName",
                table: "#detailTable",
                columns: [],
                sortName: "",
                key: ""
            });
            return {
                table,
                extend,
                editFormFields,
                editFormOptions,
                searchFormFields,
                searchFormOptions,
                columns,
                detail,
            };
        },
    });
</script>
