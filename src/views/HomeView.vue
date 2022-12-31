<template>
  <div>
    <HomeSidebar></HomeSidebar>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import HomeSidebar from '../components/HomeSidebar.vue'

export default defineComponent({
  name: 'HomeView',
  components: {
    HomeSidebar

  }
})
</script>
