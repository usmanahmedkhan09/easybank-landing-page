<template>
  <header class="header">
    <div class="icon_wrapper">
      <logoIconVue class="icon" />
    </div>
    <nav>
      <ul role="list">
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
        <li>Blog</li>
        <li>Careers</li>
      </ul>
    </nav>
    <button class="btn">Request Invite</button>
  </header>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import logoIconVue from "../icons/logoIcon.vue";

export default defineComponent({
  components: { logoIconVue },
  setup() {
    return {};
  },
});
</script>
