<template>
<div id="merchantIndex">
  <el-row :gutter="20">
    <el-col :span="8">
      <box-info id="newOrders" :info='briefInfo[0]'></box-info>
    </el-col>
    <el-col :span="8">
      <box-info id="income" :info='briefInfo[1]'></box-info>
    </el-col>
    <el-col :span="8">
      <box-info id="notifications" :info='briefInfo[2]'></box-info>
    </el-col>
  </el-row>
  <line-chart></line-chart>
</div>

</template>

<script>
import lineChart from './LineChart.vue'
import boxInfo from './BoxInfo.vue'

export default{
  components:{
    'line-chart':lineChart,
    'box-info': boxInfo
  },
  data:function(){
    return{
      briefInfo:[
        {icon:'fas fa-truck cardIcon', description:'Νέες παραγγελιες', value:'5'},
        {icon:'fas fa-money-check cardIcon', description:'Έσοδα', value:'€0.00'},
        {icon:'far fa-bell cardIcon', description:'Νέες ειδοποιήσεις', value:'0'}
      ]
    }
  },
  methods:{

  }
}

</script>

<style>
#newOrders{
  background-color: #409EFF;
  margin-left: 7%;
  margin-right: 1%;
}
#income{
  background-color: #28a745;
  margin: 0 1%;
}
#notifications{
  background-color: orange;
  margin-right: 7%;
  margin-left: 1%;
}
#merchantIndex{
  margin-top: 1%;
}

.cardIcon{
  font-size: 40px;
  color: white;
}
.cardDetails{
  font-size: 20px;
  text-align: right;
  color: white;
}
</style>
