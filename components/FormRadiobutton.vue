<template>
<div id="formRadiobutton">
    <label>{{formRadioButton.label}}</label>
    <el-radio-group v-model="resource">
      <el-radio v-for="option in formRadioButton.options" :label='option'></el-radio>
    </el-radio-group>
</div>
</template>

<script>
export default{
  props:['formRadioButton'],
  data(){
    return{
      resource:''
    }
  }
}
</script>

<style></style>
