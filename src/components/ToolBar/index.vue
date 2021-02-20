<template>
  <div class="tool_bar">
    ToolBar
    <canvas id="canvas" ref="canvas" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
class ToolBar extends Vue {
  mounted() {
    this.$message("这是一条消息提示");
    this.CanvasInt();
  }

  CanvasInt() {
    const canvas = this.$refs.canvas;
    console.log(canvas);
  }
}

export default ToolBar;
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>
