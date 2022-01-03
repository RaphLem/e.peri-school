<template>
  <div v-show="visible" ref="dest"
  :style="{
  position : 'absolute',
  top: top+'px',
  left : left+'px',
  }">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto eum facere fugit labore modi non, nulla pariatur quaerat repellendus soluta!</p>
  </div>
</template>

<script>
export default {
  name: "Contact",
}
</script>

<style scoped>

</style>