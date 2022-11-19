<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <el-button type="primary" @click="click">test</el-button>
    <el-button type="text" @click="dialogVisible = true">点击打开 Dialog</el-button>

    <el-dialog title="提示" v-if="dialogVisible" :visible.sync="dialogVisible" width="30%">
      <ChildDemo1 type="basic" />
      <ChildDemo1 type="business" />
      <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import ChildDemo1 from "@/components/childDemo1.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld,
    ChildDemo1
  },
  data() {
    return {
      dialogVisible: false
    };
  },
  methods: {
    click() {
      console.log(1);
    }
  }
};
</script>
