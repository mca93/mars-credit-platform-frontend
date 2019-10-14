<template>
  <el-row :gutter="20">
    <el-col :span="4">
      <div class="grid-content bg-purple">
        <el-select v-model="value" placeholder="Select Card Status">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          ></el-option>
        </el-select>
      </div>
    </el-col>
    <el-col :span="16">
      <div class="grid-content bg-purple">
        <el-input placeholder="Please client's name" v-model="input"></el-input>
      </div>
    </el-col>
    <el-col :span="4">
      <div class="grid-content bg-purple">
        <el-button type="primary">Search</el-button>
      </div>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data() {
    return {
      options: [
        {
          value: "Option1",
          label: "Option1"
        },
        {
          value: "Option2",
          label: "Option2"
        },
        {
          value: "Option3",
          label: "Option3"
        },
        {
          value: "Option4",
          label: "Option4"
        },
        {
          value: "Option5",
          label: "Option5"
        }
      ],
      value: ""
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../../assets/scss/_variables";
</style>

