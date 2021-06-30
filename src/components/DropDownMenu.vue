<template>
  <div style="color: black">
    <select @change="commandChange" v-model="selectedCommand">
      <option value=""><slot></slot></option>
      <option value="logout">Logout</option>
      <option value="other">Other</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "DropDownMenu",
  components: {},
  props: {},
  data() {
    return {
      selectedCommand: "",
      logout: "logout",
      other: "other",
    };
  },
  mounted() {},
  beforeDestroy() {},
  methods: {
    commandChange() {
      this.$emit("command-change", this.selectedCommand);
    },
  },
};
</script>

<style lang="css" scoped>
</style>
