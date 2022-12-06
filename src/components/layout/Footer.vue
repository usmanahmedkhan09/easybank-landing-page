<template>
  <footer class="footer">
    <div class="logo_wrapper">
      <Logo class="logo" />
      <div class="social-icons">
        <IconYouTube />
        <IconFaceBook />
        <IconTwitter />
        <IconInstagram />
        <IconPrinterest />
      </div>
    </div>
  </footer>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import Logo from "@/components/icons/logoIcon.vue";
import IconYouTube from "@/components/icons/icon-youtube.vue";
import IconFaceBook from "@/components/icons/icon-facebook.vue";
import IconTwitter from "@/components/icons/icon-twitter.vue";
import IconInstagram from "@/components/icons/icon-instagram.vue";
import IconPrinterest from "@/components/icons/icon-pinterest.vue";

export default defineComponent({
  components: {
    Logo,
    IconYouTube,
    IconFaceBook,
    IconTwitter,
    IconInstagram,
    IconPrinterest,
  },
  setup() {
    return {};
  },
});
</script>
