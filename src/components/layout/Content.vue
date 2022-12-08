<template>
  <main class="content">
    <div class="content--intro">
      <div class="details">
        <h1>Next generation digital banking</h1>
        <p>
          Take you financial life online.Your Easy bank account will be
          one-stop-shop for spending, saving, budgeting,investing,and much more
        </p>
        <button class="btn">Request invite</button>
      </div>
      <div class="icon_wrapper">
        <img class="image" src="../../assets/images/image-mockups.png" alt="" />
      </div>
    </div>
    <!-- <onboardingVue />
    <articlesVue /> -->
  </main>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import onboardingVue from "./reuseable/onboarding.vue";
import articlesVue from "./reuseable/articles.vue";

export default defineComponent({
  components: { onboardingVue, articlesVue },
  setup() {
    return {};
  },
});
</script>
