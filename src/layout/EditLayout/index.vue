<template>
  <div class="edit_layout">
    <section class="top">
      <slot name="edit_top" />
    </section>
    <section class="bottom">
      <section class="left">
        <slot name="edit_left" />
      </section>
      <section class="middle">
        <slot name="edit_middle" />
      </section>
      <section class="right">
        <slot name="edit_right" />
      </section>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {},
})
class EditLayout extends Vue {}

export default EditLayout;
</script>

<style lang="scss" scoped>
.edit_layout {
  height: 100%;
  display: flex;
  flex-direction: column;
  .top {
    flex-grow: 0;
    flex-shrink: 1;
  }
  .bottom {
    flex: 1;
    background: pink;
    display: flex;
    .left,
    .right {
      flex-grow: 0;
      flex-shrink: 1;
    }
    .middle {
      flex: 1;
    }
  }
}
</style>
