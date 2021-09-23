<template>
  <div>
      <ul>
          <li class="grid grid-cols-1 lg:grid-cols-2">
              <div>时间</div>
              <div>
              <div>标题</div>
              <div>标签</div>
              <div>正文</div>
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

        }
    }
}
</script>

<style>

</style>