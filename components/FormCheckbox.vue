<template>
<div id="formCheckbox">
  <label>{{formCheckbox.label}}</label>
  <el-checkbox-group v-model="type">
    <el-checkbox v-for="option in formCheckbox.options" :label="option" name="type"></el-checkbox>
  </el-checkbox-group>
</div>
</template>

<script>
export default{
  props:['formCheckbox'],
  data(){
    return{
      label:'',
      type:[]
    }
  }
}
</script>

<style></style>
