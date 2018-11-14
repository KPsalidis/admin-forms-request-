<template>
  <div>
    <el-row id="merchNavbar">
      <el-col :span="2">
        <div class="grid-content">
          <el-button id="sidebarToggle">
            <i class="fas fa-align-justify"></i>
          </el-button>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="grid-content" id="logo">
          Gooda
        </div>
      </el-col>

      <el-col :span="16">
        <div class="grid-content">
          <el-badge :value="2" class="item" type="danger" id="bellBadge">
            <i id="notificationBell" class="el-icon-bell"></i>
          </el-badge>
        </div>
      </el-col>

      <!-- <el-col :span="2">
        <div class="grid-content">
          <el-button id="sidebarToggle">
            <i class="fas fa-align-justify"></i>
          </el-button>
        </div>
      </el-col> -->

    </el-row>
    <hr>
  </div>
</template>

<script>

export default{
  data(){
    return{

    }
  },
  methods:{

  }
}

</script>

<style>
#bellBadge{
  float: right;
  margin: 1% 5% 0% 0%;

}
#merchNavbar{
  padding: 1% 0%;
}
#logo{
  font-size: 35px;
  color:orange;
}
#sidebarToggle{
  margin-left: 15%;
  height: 40px;
  border: none;
  font-size: 30px;
}
#notificationBell{
  float: right;
  font-size: 25px;
  color:black;
}
</style>
