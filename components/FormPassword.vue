<template>
  <div id="passwordForm">
    <label>{{formPasswordDetails.label}}</label>
    <el-input type="password" v-model="input" :required='formPasswordDetails.required'></el-input>
  </div>
</template>


<script>
export default{
  props:['formPasswordDetails'],
  data(){
    return{
      input:''
    }
  }
}
</script>
<style></style>
