<script setup>
import { ref } from 'vue';

const paths = [
  [
    "/ours-result/ours-blackswan.mp4", 
    "Different Subject", 
    "Source: Black Swan",
    "Edit: Horse",
    "Edit: Gray Bus",
    "Edit: Gray Car",
  ],
  [
    "/ours-result/ours-man.mp4", 
    "Multi Subject", 
    "Source: Man",
    "Edit: Horse",
    "Edit: Horse with Man",
    "Edit: Plane",
  ],
  [
    "/ours-result/ours-jellyfish.mp4", 
    "Style Editing", 
    "Source: Jellyfish",
    "Edit: Shark",
    "Edit: Fish with Animate Style",
    "",
  ],
  [
    "/ours-result/ours-cow.mp4", 
    "Background Editing", 
    "Source: Cow",
    "Edit: Crocodile",
    "Edit: Crocodile in Puddle",
    ""
  ],
  [
    "/ours-result/ours-rocket.mp4", 
    "Different Size", 
    "Source: Rocket",
    "Edit: Small Bird",
    "Edit: Big Bird",
    ""
  ],
  [
    "/ours-result/ours-ship.mp4", 
    "Others", 
    "Source: Ship",
    "Edit: Car",
    "",
    "",
  ],
]
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">More Ours Results</h1>
    </el-row>

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="18" :lg="16" :xl="14">
          <el-row justify="space-around">
            <el-col :span="24" v-for="(path, index) in paths" :key="index">
              <h3 style="margin: 0px 0px 10px 0px;">⬇️ {{path[1]}}</h3>
              <video muted autoplay playsinline loop>
                <source :src="path[0]" type="video/mp4">
              </video>
              <el-row justify="space-around" style="margin-top: -10px;">
                <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{path[2]}}</p>
                <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{path[3]}}</p>
                <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{path[4]}}</p>
                <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{path[5]}}</p>
              </el-row>
              <el-divider style="margin: -10px 0px 20px 0px;" v-if="index !== paths.length - 1"/>
            </el-col>
          </el-row>
        </el-col>
    </el-row>

  </div>
</template>

<style scoped>
iframe, video {
  width: 100%;
}

.el-row {
  margin-bottom: 20px;
}
.el-row:last-child {
  margin-bottom: 0;
}
.el-col {
  border-radius: 4px;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
  background: black;
}
</style>
