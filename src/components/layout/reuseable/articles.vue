<template>
  <div class="content--articles">
    <h4 class="title">Latest Articles</h4>
    <div class="aticles_wrapper">
      <div class="article" v-for="(article, index) in articles" :key="index">
        <div class="article--header">
          <img :src="getImageUrl(article.pic)" alt="" />
        </div>
        <div class="article--body">
          <p class="author">By {{ article.author }}</p>
          <p class="title">{{ article.title }}</p>
          <p class="des">{{ article.details }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const articles = ref([
      {
        author: "Calire Robinson",
        pic: "currency",
        title: "Receive money in any currency with no fees",
        details:
          "The world is getting smaller and we're becoming more mobile.So why you should be forced to only recive money in a single...",
      },
      {
        author: "Wilson Hutton",
        pic: "restaurant",
        title: "Treat yourself without worrying about money",
        details:
          "Our simple budgeting feature allow you to seperate out your spending and set realistic limits each month.Thats means you...",
      },
      {
        author: "Wilson Hutton",
        pic: "plane",
        title: "Take your EasyBank card where you go",
        details:
          "We want you to enjoy your travels.This is why we don't charge any fees on purchase while you're abroad.We'll even show you...",
      },
      {
        author: "Calire Robinson",
        pic: "confetti",
        title: "Our invite-only Beta accounts are now live!",
        details:
          "After a lot of hard work by the whole team, we're excited to lunch our closed beta.It's easy to request an invite through the site...",
      },
    ]);

    const getImageUrl = (name: any) => {
      return new URL(
        `../../../assets/images/image-${name}.jpg`,
        import.meta.url
      ).href;
    };

    return {
      articles,
      getImageUrl,
    };
  },
});
</script>
