<template>
  <div id="lineChart">
    <el-card>
      <el-row>
        <el-col :span="4">
          <h4>Έσοδα</h4>
          <p>Νοεμβριος 2014</p>
        </el-col>
        <el-col :span="20" id="timeFilter">

          
          <el-radio-group v-model="timeRadioButton" size="medium">
            <el-radio-button label="Ημέρα"></el-radio-button>
            <el-radio-button label="Εβδομάδα"></el-radio-button>
            <el-radio-button label="Μήνας" ></el-radio-button>
          </el-radio-group>


        </el-col>
      </el-row>
    </el-card>
  </div>
</template>


<script>

export default{
  data(){
    return {
      timeRadioButton:'Μήνας'
    }
  },
  methods:{

  }
}

</script>


<style>
#timeFilter{
  text-align: right;
}
#lineChart{
  margin:1% 2.3%;
}
</style>
