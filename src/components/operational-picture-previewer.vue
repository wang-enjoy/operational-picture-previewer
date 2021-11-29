<script>
import { reactive, ref, toRefs } from 'vue'
export default {
  props: {
    msg: String
  },
  setup(props) {
    const state = reactive({
      msg: props.msg,
      count: 0,
      name: 'wang'
    })
    return {
      ...toRefs(state)
    }
  }
}

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
</template>

<style scoped>
</style>
