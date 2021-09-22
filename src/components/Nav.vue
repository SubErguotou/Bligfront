<template>
  <nav class="flex h-36  py-10 items-center justify-between">
    <div class="flex w-48 justify-between items-center">
      <h1 class="max-h-14 w-14">
        <img
          src="../assets/image/QQ图片20210922092658.jpg"
          alt=""
          class="max-w-full max-h-full"
        />
      </h1>
      <p class="h-6 text-2xl font-semibold">二锅头blog</p>
    </div>
    <ul class="flex max-h-14">
      <li v-for="(item, index) in TagsList" :key="index">
        <a href="#" class="p-1 md:p-4 font-medium text-gray-900">{{
          item.name
        }}</a>
      </li>
      <button class="max-h14 mx-3">
        <svg
          t="1632285725652"
          class="icon"
          viewBox="0 0 1024 1024"
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          p-id="2970"
          width="24"
          height="24"
        >
          <path
            d="M688.2 703.5c-204.6 0-370.4-165.8-370.4-370.4 0-67.7 18.2-131.1 49.9-185.7C237 208.2 146.5 340.6 146.5 494.2c0 211.2 171.2 382.4 382.4 382.4 155.1 0 288.7-92.4 348.7-225.1-55.5 33-120.2 52-189.4 52z"
            p-id="2971"
          ></path>
        </svg>
      </button>
    </ul>
  </nav>
</template>

<script>
import { reactive } from "vue";
export default {
  setup() {
    const TagsList = reactive([
      { id: 1, name: "Blog" },
      { id: 2, name: "Tags" },
      { id: 3, name: "About" },
    ]);
    return {
      TagsList,
    };
  },
};
</script>

<style scope lang="postcss">
/* .btn {
    @apply py-2 px-4 font-semibold rounded-lg shadow-md;
  }
  .btn-green {
    @apply text-white bg-green-500 hover:bg-green-700;
  } */
</style>