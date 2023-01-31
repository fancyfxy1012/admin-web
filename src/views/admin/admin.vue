<template>
    <div class="admins" style="margin-left:">
        <div>
        <el-button icon="el-icon-search" circle style="margin-left:30%"></el-button>
    <el-input v-model="input" placeholder="请输入内容" style="width:30%;margin-left:3%;margin-top:5%;margin-right:2%"></el-input>
    <el-divider><i class="el-icon-apple"></i></el-divider>
   
   <el-table
    :data="tableData"
    border
    style="width:55%;margin-left:20%;margin-top:3%">
    <el-table-column
      fixed
      prop="date"
      label="编号"
      width="100">
    </el-table-column>
    <el-table-column
      prop="name"
      label="农产品图片"
      width="120">
    </el-table-column>
    <el-table-column
      prop="province"
      label="名称"
      width="100">
    </el-table-column>
    <el-table-column
      prop="city"
      label="标签"
      width="100">
      上架
      <el-switch
  v-model="value"
  active-color="#13ce66"
  inactive-color="#ff4949">
</el-switch>
新品
<el-switch
  v-model="value"
  active-color="#13ce66"
  inactive-color="#ff4949">
</el-switch>
推荐
      <el-switch
  v-model="value"
  active-color="#13ce66"
  inactive-color="#ff4949">
</el-switch>
    </el-table-column>
    <el-table-column
      prop="address"
      label="审核状态"
      width="100">
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
    </div>
</template>

<script>
import Jurisdiction from '../../components/Jurisdiction'
export default {
    methods: {
      handleClick(row) {
        console.log(row);
      }
    },

    data() {
      return {
        tableData: [{
          date: '1',
          name: '',
          province: '小麦',
          city: '',
          address: '未审核',
          zip: 200333
        }, {
          date: '2',
          name: '',
          province: '水稻',
          city: '',
          address: '未审核',
          zip: 200333
        },]
    }
}
}
</script>


<style lang="less" scoped>

</style>