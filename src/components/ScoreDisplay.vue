<template>
  <div class="display inline">
    <h1 class="count">0</h1>
    <h3 class="label">RECORDE</h3>
  </div>
</template>

<script>
export default {
  name: 'ScoreDisplay',
}

</script>
<style scoped>
  .display {
    margin-top: -10px;
    position: relative;
    text-align: center;
  }
  .count {
    color: #DC0D29;
    padding: 0;
    font-size: 2em;
    width: 140px;
    background-color: #32050C;
    position: relative;
    border: 4px solid #222;
    border-radius: 10px;
    margin: auto;
  }
  .label {
    color: #222;
    font-size: 0.7em;
    margin-top: 5px;
    text-align: center;
  }
</style>
