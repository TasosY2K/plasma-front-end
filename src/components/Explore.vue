<template>
  <div class="explore-container">
    <Card/>
  </div>
</template>

<script>
import Card from '@/components/Card'
export default {
  name: 'Explore',
  components: {
    'Card': Card
  }
}
</script>

<style scoped>
.explore-container {
  color: #fff;
}
</style>
