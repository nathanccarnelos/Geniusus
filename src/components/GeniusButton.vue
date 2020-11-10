<template>
  <div :class="`button ${buttonColor} ${activate ? 'active' : ''}`"
       @mousedown="changeActive"
       @touchstart="changeActive"
       @mouseup="activate=false"
       @touchend="activate=false"
       @touchout="activate=false"
       @mouseout="activate=false">
  </div>
</template>

<script>
export default {
  name: 'GeniusButton',
  props: {
    buttonColor: String
  },
  data() {
    return {
      activate: false
    }
  },
  methods: {
    changeActive() {
      this.activate = true
    }
  }
}

</script>
<style scoped>
  .button{
    position: relative;
    width: 200px;
    height: 200px;
    background-color: grey;
    border: 12px solid #333;
    display: inline-block;
  }
  .blue {
    background-color: #094a8f;
    border-bottom-right-radius: 100%;
  }
  .blue.active {
    background-color: #1c8cff;
  }
  .green{
    background-color: #00a74a;
    border-top-left-radius: 100%;
  }
  .green.active {
    background-color: #13ff7c;
  }
  .red{
    background-color: #9f0f17;
    border-top-right-radius: 100%;
  }
  .red.active {
    background-color: #ff4c4c;
  }
  .yellow{
    background-color: #cca707;
    border-bottom-left-radius: 100%;
  }
  .yellow.active {
    background-color: #fed93f;
  }
</style>
