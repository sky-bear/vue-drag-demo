<template>
  <section class="painter" @drop="drop($event)" @dragover="allowDrag($event)">
    <div>
      画布
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
class Painter extends Vue {
  drop(ev: any) {
    console.log(ev);
    ev.preventDefault();
    var data = ev.dataTransfer.getData("Text");
    console.log(data, 55);
    // ev.target.appendChild(document.getElementById(data));
  }
  allowDrag(ev: any) {
    ev.preventDefault();
  }
}
export default Painter;
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>
