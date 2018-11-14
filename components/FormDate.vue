<template>
<div id="formDate">
  <label>{{label}}</label>
  <el-date-picker type="date" v-model='date' :placeholder='placeholder'></el-date-picker>
</div>
</template>

<script>
export default{
  data(){
    return{
        date:'',
        placeholder:'Pick a date',
        label:''
    }
  }
}
</script>
<style></style>
