<template>
  <div class="side_menu">
    <input type="text" v-model="childText" />
    <button @click="sendParent">親に送る</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      childText:""
    };
  },
  methods: {
    sendParent() {
      this.$emit("getChildText", this.childText);
      this.childText = "";
    }
  }
};
</script>

