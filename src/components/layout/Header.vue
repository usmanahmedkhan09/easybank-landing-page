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
    <MenuIcon
      v-if="!showSidebar"
      @click="showSidebar = true"
      class="menuIcon"
    />
    <CloseIcon v-else @click="showSidebar = false" class="menuIcon" />
  </header>
  <SidebarVue class="sidebar" v-if="showSidebar" />
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import logoIconVue from "../icons/logoIcon.vue";
import MenuIcon from "../icons/hamburgerIcon.vue";
import SidebarVue from "./Sidebar.vue";
import CloseIcon from "../icons/closeIcon.vue";

export default defineComponent({
  components: { logoIconVue, MenuIcon, SidebarVue, CloseIcon },
  setup() {
    const showSidebar = ref(false);
    return {
      showSidebar,
    };
  },
});
</script>
