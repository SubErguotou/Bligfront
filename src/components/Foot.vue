<template>
  <footer>
    <div class="flex flex-col items-center space-y-4 py-16 sm:pt-20 sm:pb-24">
      <div class="flex flex-row space-x-5">
        <a v-for="(item, index) in LinkIcon" :key="index" :href="item.data.link">
          <img :src="'/src/assets/image/icon/'+ item.data.icon" alt="" class="w-6 h-6" />
        </a>
      </div>
      <div class="mb-2 space-x-2 text-sm text-gray-500">
          <span>Erguotou</span>
          <span> • </span>
          <span>© 2021</span>
          <span> • </span>
          <span>二锅头</span>
      </div>
      <div class="mb-8 text-sm text-gray-500">
          <a href="">
              Tailwind Nextjs Theme
          </a>
      </div>
    </div>
  </footer>
</template>

<script>
import { reactive } from "vue";
export default {
  setup() {
    const LinkIcon = reactive([
      {
        data: {
          name: "知乎",
          link: "https://www.zhihu.com/",
          icon: "知乎.svg",
        },
      },
      {
        data: {
          name: "github",
          link: "https://www.zhihu.com/",
          icon: "github.svg",
        },
      },
      {
        data: {
          name: "bilibili",
          link: "https://www.zhihu.com/",
          icon: "bilibili.svg",
        },
      },
    ]);
    return {
      LinkIcon,
    };
  },
};
</script>

<style>
</style>