<template>
    <el-card class="box-card">
      <el-row>
        <el-col :span="4">
          <i :class="info.icon"></i>
        </el-col>
        <el-col :span="20" class="cardDetails">
          <h2>{{info.value}}</h2>
          <p>{{info.description}}</p>
        </el-col>
      </el-row>
    </el-card>
</template>


<script>
export default{
  props:{
    info:{
      type:Object,
      requred:false
    }
  },
  data(){
    return{

    }
  }
}
</script>


<style>
</style>
