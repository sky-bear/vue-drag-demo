<template>
  <section class="components_list">
    <div>组件列表</div>
    <div id="drag1" draggable="true" @dragstart="drag($event)">托转测试</div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
class ComponentsList extends Vue {
  drag(ev: any) {
    ev.dataTransfer.setData("Text", ev.target.id);
    console.log(ev);
  }
}
export default ComponentsList;
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>
