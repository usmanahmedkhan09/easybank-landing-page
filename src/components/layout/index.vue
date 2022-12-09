<template>
  <HeaderVue />
  <ContentVue />
  <FooterVue />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HeaderVue from "./Header.vue";
import ContentVue from "./Content.vue";
import FooterVue from "./Footer.vue";

export default defineComponent({
  components: { HeaderVue, ContentVue, FooterVue },
  setup() {
    return {};
  },
});
</script>
