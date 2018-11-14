<template>
  <div id="formTextarea">
    <label>{{formTextarea.label}}</label>
    <el-input type="textarea" v-model="desc"></el-input>
  </div>
</template>

<script>
export default{
  props:['formTextarea'],
  data(){
    return{
      desc:''
    }
  }
}
</script>

<style></style>
