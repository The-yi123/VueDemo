<template>
  <div class="hello">
    姓：
    <input v-model="firstName" />
    名：
    <input v-model="lastName" />
    全称姓名：<span>{{fullName}}</span>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      firstName: "",
      lastName: ""
    };
  },
  computed: {
      fullName: function() {
        return this.firstName + "  " + this.lastName;
      }
  },
  watch:{
    firstName:function(){
      this.firstName+"我是watch监听过后的数据内容"
      console.log("watch监听生效")
    }
  }
};
</script>
