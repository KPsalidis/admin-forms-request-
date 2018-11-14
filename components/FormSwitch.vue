<template>
  <div id="formSwitch">
    <label>{{formSwitch.label}}</label>
    <el-switch v-model="button"></el-switch>
  </div>
</template>

<script>
export default{
  props:['formSwitch'],
  data(){
    return{
      label:'label 123',
      button:false
    }
  }
}
</script>

<style></style>
