<template>
  <div>
      <Search :msg="msg" />
      <ul>
          <li class="grid grid-cols-1 lg:grid-cols-4 py-4 shadow-sm" v-for="(item, index) in BlogList" :key="index">
              <div class="text-base font-medium leading-6 text-gray-500 my-2">{{item.data.time}}</div>
              <div class="lg:col-span-2">
                <div class="text-gray-900 truncate text-2xl font-bold leading-8 tracking-tight">{{item.data.title}}</div>
                <div class="mr-3 text-sm font-medium text-blue-400 uppercase hover:text-blue-600">{{item.data.tag}}</div>
                <div class="pt-3 prose text-gray-500">{{item.data.text}}</div>
              </div>
          </li>
      </ul>
      <page />
  </div>
</template>

<script>
import {reactive, ref} from'vue'
import Page from './propscomponent/page.vue'
import Search from '../components/propscomponent/Search.vue'
export default {
    components: {
        Page,
        Search
    },
    setup() {
        let msg = ref('All Posts')
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
                    text:'Flex 布局是轴线布局，只能指定"项目"针对轴线的位置，可以看作是一维布局。Grid 布局则是将容器划分成"行"和"列"，产生单元格，然后指定"项目所在"的单元格，可以看作是二维布局。Grid 布局远比 Flex 布局强大。',
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
            msg
        }
    }
}
</script>

<style>

</style>