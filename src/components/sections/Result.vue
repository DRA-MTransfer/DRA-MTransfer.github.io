<script setup>
import { ref } from 'vue';

const image_paths = [
    ["./result/swan-horse-car.gif", "Different Subject", "Black Swan (GT) - Horse - Bus - Car"],
    ["./result/man-horse.gif", "Multi Subject", "Man (GT) - Horse - Horse with Man"],
    ["./result/jellyfish-fish.gif", "Style Editing", "Jelly Fish (GT) - Shark - Fish with Animate Style"],
    ["./result/cow-crocodile.gif", "Background Editing", "Cow (GT) - Crocodile - Crocodile in Puddle"],
    ["./result/rocket-bird.gif", "Different Size", "Rocket (GT) - Small Bird - Big Bird"],
  ]
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">More Results</h1>
    </el-row>

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12" >
          <el-row justify="space-around">
            <el-col :span="24" v-for="path in image_paths" >
              <h3 style="margin-bottom: 4px;">⬇️ {{path[1]}}</h3>
              <p style="margin: 4px;">{{path[2]}}</p>
              <el-row justify="space-around">
                <el-image :src="path[0]"/>
              </el-row>
            </el-col>
          </el-row>
        </el-col>
    </el-row>

  </div>
</template>

<style scoped>
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