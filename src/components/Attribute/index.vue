<template>
  <div class="attribute">
    属性区域
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
class Attribute extends Vue {}
export default Attribute;
</script>

<style lang="scss" scoped>
@import "./index.scss";
</style>
