<template>
  <div>
      <div class="grid grid-cols-1 sm:grid-cols-4 mt-8 md:mt-16">
        <div class="sm:col-start-2 sm:col-end-2 pr-8 text-2xl font-extrabold font-serif md:text-4xl md:place-self-end">
          Tags
        </div>
        <div class="flex flex-wrap content-center sm:col-start-3 sm:col-end-3 sm:pl-8 border-gray-200 md:border-l-2">
          <span class="" v-for="(item, index) in tags" :key="index">{{item}}</span>
        </div>
      </div>
  </div>
</template>

<script>
import {ref} from "vue"
export default {
  setup() {
    const tags = ref(["life", "code", "node"])
    return {
      tags
    }
  }
}
</script>

<style>

</style>