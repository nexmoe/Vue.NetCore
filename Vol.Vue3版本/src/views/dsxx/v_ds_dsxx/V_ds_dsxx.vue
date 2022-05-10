<!--
*Author：jxx
 *Contact：283591387@qq.com
 *代码由框架生成,任何更改都可能导致被代码生成器覆盖
 *业务请在@/extension/system/v_ds_dsxx/V_ds_dsxx.js此处编写
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
    import extend from "@/extension/dsxx/v_ds_dsxx/V_ds_dsxx.js";
    import { ref, defineComponent } from "vue";
    export default defineComponent({
        setup() {
            const table = ref({
                key: 'id',
                footer: "Foots",
                cnName: '导师视图',
                name: 'v_ds_dsxx/V_ds_dsxx',
                url: "/V_ds_dsxx/",
                sortName: "dsbh"
            });
            const editFormFields = ref({});
            const editFormOptions = ref([]);
            const searchFormFields = ref({});
            const searchFormOptions = ref([]);
            const columns = ref([{field:'dsbh',title:'导师编号',type:'string',sort:true,width:110,require:true,align:'left',sort:true},
                       {field:'dsxm',title:'导师姓名',type:'string',sort:true,width:110,align:'left'},
                       {field:'xb',title:'性别',type:'string',width:110,align:'left'},
                       {field:'xsmc',title:'学院',type:'string',width:110,align:'left'},
                       {field:'yddh',title:'手机',type:'string',width:110,align:'left'},
                       {field:'dwdh',title:'单位电话',type:'string',width:110,align:'left'},
                       {field:'zzdh',title:'住宅电话',type:'string',width:110,align:'left'},
                       {field:'GBZW',title:'职务',type:'string',width:110,align:'left'},
                       {field:'csrq',title:'出生日期',type:'string',width:110,align:'left'},
                       {field:'zcmc',title:'职称',type:'string',width:110,align:'left'},
                       {field:'MZ',title:'民族',type:'string',width:110,align:'left'},
                       {field:'zzmm',title:'政治面貌',type:'string',width:110,align:'left'},
                       {field:'role',title:'角色',type:'string',width:110,align:'left'},
                       {field:'pzsdny',title:'聘任硕导年月',type:'string',width:110,align:'left'},
                       {field:'pzbdny',title:'聘任博导年月',type:'string',width:110,align:'left'},
                       {field:'hxwyx',title:'hxwyx',type:'string',width:110,align:'left'},
                       {field:'hxwsj',title:'hxwsj',type:'string',width:110,align:'left'},
                       {field:'hxlyx',title:'hxlyx',type:'string',width:110,align:'left'},
                       {field:'hxlsj',title:'hxlsj',type:'string',width:110,align:'left'},
                       {field:'yjfx',title:'研究方向',type:'string',width:120,align:'left'},
                       {field:'bz',title:'备注',type:'string',width:110,align:'left'},
                       {field:'dslb',title:'导师类别',type:'string',width:110,align:'left'},
                       {field:'yjxkdm',title:'一级学科代码',type:'string',width:110,align:'left'},
                       {field:'yjxk',title:'一级学科',type:'string',width:110,align:'left'},
                       {field:'zylydm',title:'专业领域代码',type:'string',width:110,align:'left'},
                       {field:'zyly',title:'专业领域',type:'string',width:110,align:'left'},
                       {field:'cszym1',title:'从事专业代码1',type:'string',width:110,align:'left'},
                       {field:'cszymc1',title:'从事专业1',type:'string',width:110,align:'left'},
                       {field:'cszym2',title:'从事专业代码2',type:'string',width:110,align:'left'},
                       {field:'cszymc2',title:'从事专业2',type:'string',width:110,align:'left'},
                       {field:'cszym3',title:'从事专业代码3',type:'string',width:110,align:'left'},
                       {field:'cszymc3',title:'从事专业3',type:'string',width:110,align:'left'},
                       {field:'id',title:'ID',type:'long',width:110,require:true,align:'left'},
                       {field:'jbqk',title:'基本情况',type:'string',width:110,align:'left'},
                       {field:'yjfxqk',title:'研究方向',type:'string',width:110,align:'left'},
                       {field:'hjqk',title:'获奖情况',type:'string',width:110,align:'left'},
                       {field:'qtqk',title:'其他情况',type:'string',width:110,align:'left'},
                       {field:'kyqk',title:'科研情况',type:'string',width:110,align:'left'},
                       {field:'AuditStatus',title:'审核状态',type:'int',width:110,align:'left'},
                       {field:'HeadImageUrl',title:'头像地址',type:'string',width:180,align:'left'},
                       {field:'email',title:'email',type:'string',width:110,align:'left'}]);
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
