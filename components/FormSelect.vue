<template>
  <div id="formSelect">
    <label>{{formSelect.label}}</label>
    <el-select :placeholder="formSelect.placeholder">
      <el-option v-for="option in formSelect.options" :value="option"></el-option>
    </el-select>
  </div>
</template>

<script>
export default{
  props:['formSelect'],
  data(){
    return{

    }
  }
}
</script>
<style></style>
