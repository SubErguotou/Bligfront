<template>
  <div>
    <Title :msg="msg" />
    <div class="flex flex-col sm:flex-row w-auto pt-6 mt-8 border-t-2">
      <div class="flex flex-col sm:w-1/4 justify-center items-center space-y-2">
        <div class="w-48 h-48">
          <img
            src="../assets/image/Snipaste_2021-09-26_10-26-59.png"
            alt=""
            class="rounded-full"
          />
        </div>
        <div class="flex flex-col justify-items items-center space-y-2">
          <p class="font-extrabold text-xl">Erguotou</p>
          <p class="text-gray-500">不知道填什么好</p>
          <div class="flex flex-row space-x-5">
            <a
              v-for="(item, index) in LinkIcon"
              :key="index"
              :href="item.data.link"
            >
              <img
                :src="'/src/assets/image/icon/' + item.data.icon"
                alt=""
                class="w-6 h-6"
              />
            </a>
          </div>
        </div>
      </div>
      <div class="flex flex-col  sm:w-3/4 mt-8 sm:mt-0 p-4 text-gray-500 text-lg space-y-4">
        <p class="">
          &nbsp; &nbsp; 北京酿制白酒的历史悠久。到了清代中期，京师烧酒作坊为了提高烧酒品质，进行了工艺改革。在蒸酒时用作冷却器的称为锡鏊，也称天锅。蒸酒时，需将蒸馏而得的酒汽，经第一次放入锡锅内的凉水冷却而流出的“酒头”和经第三次换入锡锅里的凉水冷却而流出的“酒尾”提出做其它处理，因为第一锅和第三锅冷却的酒含有多种低沸点的物质成分，味道较杂，所以酒厂只摘取味道醇厚的经第二次换入锡锅里的凉水冷却而流出的酒，故起名为“二锅头”。
        </p>
        <p>
         &nbsp; &nbsp; 锡鏊其实就是冷却器，因器锡制，其状敞口圆形、二十公分以下，45度角向圆心倾斜，收缩至锥尖，类似鼓鏊，故名，内容冷水。原理为：当酒醅加热汽徐徐上升，遇之骤冷，变为露酒，沿锡熬外壁滴淌汇入下面承露盘，通过连接承露盘之锡管，如线泉般流出，淌突至蒸馏锅外藤条酒篓子。
        </p>
        <p>
        &nbsp; &nbsp;因天锅容积有限，火（古为炉火)或汽(今为蒸汽)不宜大，缓火蒸馏，并不断搅拌天锅盛水，控制流酒温度。
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
import Title from "../components/propscomponent/Title.vue";
export default {
  setup() {
    let msg = ref("About");
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
      msg,
      LinkIcon,
    };
  },
  components: {
    Title,
  },
};
</script>

<style>
</style>