<script>
import { Swiper, SwiperSlide} from 'swiper/vue';
import { Navigation, Autoplay, Scrollbar, EffectFade } from 'swiper/modules';
import 'swiper/css/bundle';

export default {
  components: {
      Swiper,
      SwiperSlide,
    },
  data() {
    return {
      modules: [
        Navigation,
        Autoplay,
        Scrollbar,
        EffectFade,
      ],
      // 选择要轮播的照片
      paths: [
        ["/traning-based-method-compare/bear-eagle.mp4", "Source: Bear → Edit: Eagle"],
        ["/traning-based-method-compare/goat-man.mp4", "Source: Goat → Edit: Man"],
        ["/traning-based-method-compare/man-horse.mp4", "Source: Man → Edit: Horse"],
        ["/traning-based-method-compare/rocket-bird.mp4", "Source: Rocket → Edit: Bird"],
        ["/traning-based-method-compare/soccerball-cat.mp4", "Source: Soccerball → Edit: Cat"],
      ],
    }
  }
}
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">More Ours Results</h1>
    </el-row>

    <el-row justify="center" style="margin-top: 20px;">
      <el-col :xs="24" :sm="20" :md="18" :lg="16" :xl="14">
        <!-- 设置轮播图：循环播放、首张图序号、响应式、导航和分页、自动播放 -->
        <swiper
          :loop="true"
          :slidesPerView="0"
          :modules="modules"
          :effect="'fade'"
          :fade-effect="{
            crossFade:true
          }"
          :navigation="{ 
            hideOnClick:true,
          }"
          :scrollbar="{
            hide: true,
            draggable: false
          }"
          :autoplay="{ 
            delay:5000,
            disableOnInteraction:false,
            pauseOnMouseEnter:true,
          }"
          >
          <swiper-slide v-for="path in paths">
            <video muted autoplay playsinline loop>
              <source :src="path[0]" type="video/mp4">
            </video>
            <p style="text-align: center; align-content: center; font-size: 13px;">{{path[1]}}</p>
          </swiper-slide>
        </swiper>
      </el-col>
    </el-row>
  </div>

</template>
  
<style>

/* 设置Swiper风格 */
.swiper {
  --swiper-theme-color: #aeaeae;
}

iframe, video {
  width: 100%;
}

</style>
  
