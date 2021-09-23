<template>
  <div>
      <ul>
          <li class="grid grid-cols-1 lg:grid-cols-4 py-4 shadow-sm" v-for="(item, index) in BlogList" :key="index">
              <div class="text-base font-medium leading-6 text-gray-500 my-2">{{item.data.time}}</div>
              <div class="lg:col-span-2">
                <div class="text-gray-900 truncate text-2xl font-bold leading-8 tracking-tight">{{item.data.title}}</div>
                <div class="mr-3 text-sm font-medium text-blue-400 uppercase hover:text-blue-600">{{item.data.tag}}</div>
                <div class="pt-3 truncate prose text-gray-500">{{item.data.text}}</div>
              </div>

          </li>
      </ul>
  </div>
</template>

<script>
import {reactive} from'vue'
export default {
    setup() {
        const BlogList = reactive([
            {
                data:{
                    time: "2021年7月21日",
                    tag:"Life",
                    title: "第一次",
                    text:"第一次正文",
                },
            },
            {
                data:{
                    time: "2021年8月21日",
                    tag:"Life",
                    title: "第二次",
                    text:"第二次正文",
                },
            },
            {
                data:{
                    time: "2021年9月21日",
                    tag:"Life",
                    title: "第三次",
                    text:"第三次正文",
                },
            },
            {
                data:{
                    time: "2021年10月31日",
                    tag:"Life",
                    title: "第四次",
                    text:"第四次正文",
                },
            }
            
        ])
        return{
            BlogList,
        }
    }
}
</script>

<style>

</style>