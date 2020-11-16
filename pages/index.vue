<template>
  <div class="container">
    <Intersect @enter="msg = 'Intersected'" @leave="msg = 'Not intersected'">
      <div>{{ msg }}</div>
    </Intersect>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
const Intersect = require('vue-intersect')

export default defineComponent({
  components: {
    Intersect,
  },
  setup() {
    return {
      msg: 'I will change',
    }
  },
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
