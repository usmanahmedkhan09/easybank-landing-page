<template>
  <HeaderVue />
  <ContentVue />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HeaderVue from "./Header.vue";
import ContentVue from "./Content.vue";

export default defineComponent({
  components: { HeaderVue, ContentVue },
  setup() {
    return {};
  },
});
</script>
