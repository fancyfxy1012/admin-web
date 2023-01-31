<!--
 * @Author: your name
 * @Date: 2019-12-18 11:29:28
 * @LastEditTime: 2019-12-18 11:30:02
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: \vue-admin\src\views\About\About.vue
 -->
<template>
    <div>
        <el-button icon="el-icon-search" circle style="margin-left:10%"></el-button>
    <el-input v-model="input" placeholder="请输入内容" style="width:30%;margin-left:1%;margin-top:5%;margin-right:2%"></el-input>
   <el-divider><i class="el-icon-user"></i></el-divider>
   <el-table
    :data="tableData"
    border
    style="width:75%;margin-left:10%;margin-top:3%">
    <el-table-column
      fixed
      prop="date"
      label="用户注册日期"
      width="150">
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名"
      width="120">
    </el-table-column>
    <el-table-column
      prop="province"
      label="省份"
      width="120">
    </el-table-column>
    <el-table-column
      prop="city"
      label="市区"
      width="120">
    </el-table-column>
    <el-table-column
      prop="address"
      label="邮箱"
      width="300">
    </el-table-column>
    <el-table-column
      prop="zip"
      label="邮编"
      width="120">
    </el-table-column>
    <el-table-column
      fixed="right"
      label="操作"
      width="100">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
        <el-button type="text" size="small">编辑</el-button>
      </template>
    </el-table-column>
  </el-table>
</div>
</template>

<script>
export default {
    methods: {
      handleClick(row) {
        console.log(row);
      }
    },

    data() {
      return {
        tableData: [{
          date: '2022-05-02',
          name: '王小虎',
          province: '四川',
          city: '宜宾市',
          address: '2624******@qq.com',
          zip: 200333
        }, {
          date: '2022-05-04',
          name: '王小虎',
          province: '四川',
          city: '乐山市',
          address: '2624******@qq.com',
          zip: 200333
        }, {
          date: '2022-05-01',
          name: '王小虎',
          province: '四川',
          city: '自贡市',
          address: '2624******@qq.com',
          zip: 200333
        }, {
          date: '2022-05-03',
          name: '王小虎',
          province: '四川',
          city: '成都市',
          address: '2624******@qq.com',
          zip: 200333
        }],
        input: ''
      }
    }
}
</script>

<style scoped>

</style>