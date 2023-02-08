<template>
  <div>
    X - {{boxX}}
    <br/>
    Y - {{boxY}}
  </div>
</template>

<script>
export default {
  name: "NewBox",
  props: {
    hasShip: Boolean,
    shipId: Number,
    wasHit: Boolean,
    boxX: Number,
    boxY: Number
  }
}
</script>

<style scoped>

</style>