<template>
  <div>
        <el-tabs type="border-card" v-model="activeName" @tab-click="handleClick">
        <el-tab-pane label="用户管理" name="first">
          <user-tab></user-tab>
        </el-tab-pane>
        <el-tab-pane label="配置管理" name="second">
          <order-tab></order-tab>
        </el-tab-pane>
        <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
        <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
        </el-tabs>
  </div>
</template>
<script>
  import userTab from '../components/userTab'
  import orderTab from '../components/orderTab' 
  export default {
    data() {
      return {
        activeName: 'second'
      };
    },
    components:{
      userTab,
      orderTab
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
        
      }
    },	
  };
</script>