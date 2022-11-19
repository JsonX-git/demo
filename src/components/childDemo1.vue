<template>
  <div style="border: solid red 1px">
    <!-- <h1>childDemo1</h1> -->
    {{ obj }}
  </div>
</template>
<script>
export default {
  props: { type: { type: String } },
  data() {
    return {
      data: { basic: "111", business: "222" }
    };
  },

  computed: {
    obj() {
      return this.data[this.type];
    }
  },
  created() {
    console.log("created", this.obj);
  },
  updated() {
    console.log("updated", this.obj);
  },
  destroyed() {
    console.log("destroyed");
  }
};
</script>
<style scoped lang="less"></style>
