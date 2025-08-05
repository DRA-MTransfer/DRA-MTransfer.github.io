<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Pipeline from './sections/Pipeline.vue'
import OursResult from './sections/Ours-Result.vue'
import CompareResult from './sections/Compare-Result.vue'

export default {
  components: {
    Title,
    Abstract,
    Pipeline,
    OursResult,
    CompareResult,
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Pipeline/>
  <OursResult/>
  <CompareResult/>
</template>