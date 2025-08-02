<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Pipeline from './sections/Pipeline.vue'
import Result from './sections/Result.vue'

export default {
  components: {
    Title,
    Abstract,
    Pipeline,
    Result,
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Pipeline/>
  <Result/>
</template>