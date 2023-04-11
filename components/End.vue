<script setup lang="ts">
import { ref } from 'vue'
const isShow1 = ref(false)
const isShow2 = ref(false)
window.addEventListener('click', () => {
  if(isShow1.value) {
    isShow2.value = true
  }
  isShow1.value = true

})
</script>

<template>
  <div class="h-full py-[20px] px-[20px] text-[14px]">
    <h2>最后</h2>
    <div class="h-full flex mt-[25px]">
      <div class="all-indent-8 leading-10">
        <p>于敏院士为了研究氢弹，放弃了光明的学术前途，甚至落下了严重的疾病</p>
        <p>
          当别人提起他是中国氢弹之父时，于敏院士婉拒说道“这是成千上万人的事业”
        </p>
        <p>
          当别人谈起隐姓埋名的那28年，他却说：“一个人的名字，早晚是要没有的，能把微薄的力量融进祖国的强盛之中，便足以自慰了”
        </p>
        <p>
          20年前，在国庆50周年群众游行的观礼台上，刚刚被授予“两弹一星”功勋奖章的于敏，
          看着空前壮大的科技方队通过广场感慨万分：“这是历史赋予我们每个科学家义不容辞的使命。”
        </p>
        <p v-if="isShow1">
          　2019年1月16日，于敏溘然长逝，享年93岁
        </p>
        <p v-if="isShow1 && isShow2" class="text-[20px] font-bold">
          而于敏的名字，将会永远被我们铭记
        </p>
      </div>
      <img class="h-5/6" src="/word.jpg" alt="" />
    </div>
  </div>
</template>
