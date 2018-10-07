<template>
  <section>
  <h1>
    {{this.yourFate}}
  </h1>
  <button @click="yourFate = 0">I will see your fate</button>
  </section>
</template>

<script>
import {sample} from 'lodash-es'
import fates from '../utils/fate_list'
export default {
  data: function () {
    return {
      result: sample(fates)
    }
  },
  computed: {
    yourFate: {
      get () {
        return this.result
      },
      set (value) {
        this.result = sample(fates)
      }
    }
  }

}
</script>

<style>

</style>
