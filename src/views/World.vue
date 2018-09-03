<template>
  <div class="world">
    <world-spinner  :width="640" :height="480"/>
  </div>
</template>

<script>
// @ is an alias to /src
import WorldSpinner from '@/components/WorldSpinner.vue'

export default {
  name: 'world',
  components: {
    'world-spinner':WorldSpinner
  }
}
</script>
