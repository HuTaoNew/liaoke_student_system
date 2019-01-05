<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <fieldset>
      <legend>拇指哥学生录入系统</legend>
      <div>
        <span>姓名：</span>
        <input type="text" placeholder="请输入姓名">
      </div>
      <div>
        <span>年龄：</span>
        <input type="text" placeholder="请输入年龄">
      </div>
      <div>
        <span>性别：</span>
        <select name id>
          <option value="男">男</option>
          <option value="女">女</option>
        </select>
      </div>
      <div>
        <span>电话：</span>
        <input type="text" placeholder="请输入电话">
      </div>

      <button type="button" @click="save()">创建新用户</button>
    </fieldset>

    <table>
      <thead>
        <tr>
          <th>姓名</th>
          <th>年龄</th>
          <th>性别</th>
          <th>电话</th>
          <th>删除</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(p, index) in persons" :key="index">
          <td> {{p.name}} </td>
          <td> {{p.age}} </td>
          <td> {{p.sex}} </td>
          <td> {{p.phone}} </td>
          <td>
            <button>删除</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "home",
  data() {
    return {
      persons: [
        { name: "张三", age: 20, sex: "男", phone: "13812347890" },
        { name: "李四", age: 45, sex: "女", phone: "12364573214" },
        { name: "王五", age: 12, sex: "女", phone: "19987461239" },
        { name: "赵六", age: 23, sex: "男", phone: "18836471290" },
        { name: "牛气", age: 32, sex: "男", phone: "13495884657" }
      ]
    };
  },
  methods:{
    save(){

    }
  }
  // components: {
  //   HelloWorld
  // }
};
</script>

<style scoped>
.home{
  margin: 50px auto;
  width: 600px;
}

fieldset{
  border: 1px solid orangered;
  margin-bottom: 30px;
}

button {
  height: 30px;
  background-color: orangered;
  color: aliceblue;
}


fieldset input{
  width: 200px;
  height: 30px;
  margin: 10px 0;
}

table {
  width: 600px;
  border: 2px solid orangered;
  text-align: center;
}

thead {
  background-color: orangered;
}
</style>
