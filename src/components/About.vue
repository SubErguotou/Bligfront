<template>
  <div>
      <Title :msg="msg" />
      <div class="flex flex-col sm:flex-row w-auto">
        <div class="flex border-red-600 border-2 sm:w-1/4 justify-center">
        <div class="w-48 h-48 rounded-full bg-blue-600">
          <!-- <img src="../assets/image/\/QQ图片20210922092658.jpg" alt="" class=""> -->
        </div>
          <p></p>
          <p></p>
          <p></p>
          <p></p>
          <p></p>
        </div>
        <div class="border-red-600 border-2 sm:w-3/4">test2</div>
      </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import Title from '../components/propscomponent/Title.vue'
export default {
  setup() {
    let msg = ref('About')
    return {
      msg,
    }
  },
  components: {
    Title,
  }
}
</script>

<style>

</style>