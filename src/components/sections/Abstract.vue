<script setup>
import abstract from '../mds/abstract.mdx';

</script>

<template>
  <div>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="18" :lg="16" :xl="14">
          <el-container class="video-container">
            <video muted preload autoplay playsinline loop>
              <source src="/ours-result/teaser-new.mp4" type="video/mp4">
            </video>
          </el-container>
      </el-col>
    </el-row>

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="18" :lg="16" :xl="14">
          <abstract />
        </el-col>
    </el-row>

  </div>
</template>

<style scoped>
.video-container{
  margin: 0px 0px 20px 0px;
}

iframe, video {
  width: 100%;
}
</style>