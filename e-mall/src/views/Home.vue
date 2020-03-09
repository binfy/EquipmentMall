<template>
  <div class="home-wrap">
    <div class="top">
      <el-row class="top-menu">
        <el-col :span="4">
          <div class="contact-info">
            <el-dropdown size="medium">
              <span class="el-dropdown-link">
                023-62896277
                <i class="el-icon-arrow-down el-icon--right"></i>
              </span>
              <el-dropdown-menu slot="dropdown">
                <el-dropdown-item>孙先生</el-dropdown-item>
                <el-dropdown-item>118669451@qq.com</el-dropdown-item>
                <el-dropdown-item>QQ2131421379</el-dropdown-item>
              </el-dropdown-menu>
            </el-dropdown>
          </div>
        </el-col>
        <el-col :span="20">
          <div class="top-menu-item">
            <div>个人中心</div>
            <el-divider direction="vertical"></el-divider>
            <div>帮助</div>
            <el-divider direction="vertical"></el-divider>
            <div>购物车</div>
            <el-divider direction="vertical"></el-divider>
            <div>登入</div>
            <el-divider direction="vertical"></el-divider>
            <div>注册</div>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="10">
          <div >
            <el-image  class="logo" 
      :src="require('@/assets/logo.png')"
      fit="contain"></el-image>
               
              
          </div>
        </el-col>
        <el-col :span="10">
          <div>
               <el-input
    placeholder="搜索" v-model="searchContent"
    >
  </el-input>
  <!-- <label :title="searchContent"></label> -->
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>


<script lang="ts">
import { Vue, Component, Prop,Model } from "vue-property-decorator";
@Component({ name: "Home", components: {} })
export default class Home extends Vue {

  private searchContent!:string;
}
</script>
<style scoped>
.home-wrap {
  width: 100%;
  margin: 0rem;
}
.top {
  height: 12.5rem;
  background-color: #1568c7;
  padding-top: 0.5rem;
}
.top-menu {
  height: 2.5rem;
  width: 100%;
}

.contact-info {
  background-color: transparent;
  display: flex;
  margin-left: 3rem;
}

.el-dropdown-link {
  cursor: pointer;
  color: white;
}
.el-icon-arrow-down {
  font-size: 12px;
}
.top-menu-item{
 display: flex;
 justify-content: flex-end;
  margin-right: 3rem;
  color: white;
  align-items: center;
}
.logo{
height: 6.25rem;
width: 14.375rem;
margin-left: 5rem;

}
</style>
