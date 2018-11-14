<template>
<div id="formTime">
  <label>{{label}}</label>
  <el-time-picker type="fixed-time" :placeholder='placeholder' v-model="time"></el-time-picker>
</div>
</template>

<script>

export default{
  data(){
    return{
      time:'',
      label:'',
      placeholder:'Pick a time'

    }
  }
}
</script>
<style></style>
