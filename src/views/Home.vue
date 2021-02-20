<template>
  <div class="home">
    <EditLayout>
      <template #edit_top>
        <ToolBar />
      </template>
      <template #edit_left>
        <ComponentsList />
      </template>
      <template #edit_middle>
        <Painter />
      </template>
      <template #edit_right>
        <Attribute />
      </template>
    </EditLayout>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import EditLayout from "@/layout/EditLayout/index.vue";
import ToolBar from "@/components/ToolBar/index.vue";
import Attribute from "@/components/Attribute/index.vue";
import Painter from "@/components/Painter/index.vue";
import ComponentsList from "@/components/ComponentsList/index.vue";

@Component({
  components: {
    EditLayout,
    ToolBar,
    Attribute,
    Painter,
    ComponentsList,
  },
})
class Home extends Vue {}

export default Home;
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
}
</style>
