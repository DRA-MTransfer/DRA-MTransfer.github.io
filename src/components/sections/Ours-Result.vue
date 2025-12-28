<script setup>
import { ref } from 'vue';

const paths = [
  [
    "IMP & Different Subject", 
    [
      [
        "/ours-result/ours-blackswan.mp4", 
        "Source: Black Swan",
        "Edit: Horse",
        "Edit: Gray Bus",
        "Edit: Gray Car",
      ],
      [
        "/ours-result/ours-jellyfish.mp4", 
        "Source: Jellyfish",
        "Edit: Turtle",
        "Edit: Whale",
        "Edit: Shark",
      ]
    ],
  ],
  [
    "IMP & Multi Subject", 
    [
      [ 
        "/ours-result/ours-horse-bird-new.mp4", 
        "Source: Man",
        "Edit: Horse",
        "Source: Birds",
        "Edit: Planes",
      ],
      [
        "/ours-result/ours-bear-dog-rabbit-bird.mp4", 
        "Source: Bear with Ball",
        "Edit: Dog with Ball",
        "Source: Two Rabbits",
        "Edit: Two Birds",
      ]
    ],
  ],
  [
    "IMP & Background Editing", 
    [
      [
        "/ours-result/ours-cow.mp4", 
        "Source: Cow",
        "Edit: Crocodile",
        "Edit: Crocodile in Puddle",
        "",
      ]
    ],
  ],
  [
    "IMP & Different Size", 
    [
      [ 
        "/ours-result/ours-rocket-new.mp4", 
        "Source: Rocket",
        "Edit: Small Bird",
        "Edit: Big Bird",
        "",
      ]
    ],
  ],
  [
    "More IMP Results", 
    [
      [ 
        "/ours-result/ours-bus-tiger-goat-eagle.mp4", 
        "Source: Bus",
        "Edit: Tiger",
        "Source: Goat",
        "Edit: Eagle",
      ],
      [
        "/ours-result/ours-car-leopard-bear-car.mp4", 
        "Source: Car",
        "Edit: Leopard",
        "Source: Bear",
        "Edit: Car",
      ]
    ],
  ],
]
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Ours Results</h1>
    </el-row>

    <el-row justify="center">
        <el-col :xs="24" :sm="20" :md="18" :lg="16" :xl="14">
          <el-row justify="space-around">
            <el-col :span="24" v-for="(path, index) in paths" :key="index">
              <h3 style="margin: 0px 0px 10px 0px;">⬇️ {{path[0]}}</h3>
              <el-row justify="center" v-for="(video, idx) in path[1]" :key="idx" style="margin: 0px;" >
                <video muted autoplay playsinline loop><source :src="video[0]" type="video/mp4"></video>
                <el-col>
                  <el-row justify="space-around">
                    <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{video[1]}}</p>
                    <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{video[2]}}</p>
                    <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{video[3]}}</p>
                    <p style="width: 24%; text-align: center; align-content: center; margin: 0; font-size: 13px;">{{video[4]}}</p>
                  </el-row>
                </el-col>
              </el-row>
              <el-divider style="margin: 20px 0px 10px 0px;" v-if="index !== paths.length - 1"/>
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
