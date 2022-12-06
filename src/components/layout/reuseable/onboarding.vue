<template>
  <div class="content--onboarding">
    <h2 class="title">Why choose EasyBank?</h2>
    <p class="subtitle">
      We larvage open banking to trun you banking account into financial hub.
    </p>
    <p class="subtitle">Control your finances like never before</p>

    <div class="options_wrapper">
      <div
        class="option"
        v-for="(option, index) in bankingOptions"
        :key="index"
      >
        <img :src="getImageUrl(option.icon)" alt="" />
        <h5 class="title">{{ option.title }}</h5>
        <p class="detail">{{ option.detail }}</p>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const bankingOptions = ref([
      {
        title: "Online Banking",
        icon: "online",
        detail:
          "Our modren and web mobile applications allow you to keep track of your finances where are you in the world",
      },
      {
        title: "Simple Budgeting",
        icon: "budgeting",
        detail:
          "See exactly where your money goes each month.Recive notifications when you're close hiting the limits",
      },
      {
        title: "Fast OnBoarding",
        icon: "onboarding",
        detail:
          "We don't do branches.Open your account in minutes online and start tacking control of your finances right away",
      },
      {
        title: "Open  API",
        icon: "api",
        detail:
          "Manage your savings, investments and pensions, and much more from one account.Tracking your money has never been easy",
      },
    ]);

    const getImageUrl = (icon: any) => {
      return new URL(`../../../assets/images/icon-${icon}.svg`, import.meta.url)
        .href;
    };

    return {
      bankingOptions,
      getImageUrl,
    };
  },
});
</script>
