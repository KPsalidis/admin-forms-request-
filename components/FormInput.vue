<template>
  <div id="simpleForm">
    <label>{{formDetails.label}}</label>
    <el-input v-model="input" :required='formDetails.required'></el-input>
  </div>
</template>


<script>
export default{
  props:['formDetails'],
  data(){
    return{
      input:''
    }
  }
}
</script>
<style></style>
