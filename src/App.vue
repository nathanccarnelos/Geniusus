<template>
  <div class="back">
    <div class="genius">
      <template v-for="(row, key) in rowsList" :key="key">
        <div class="row">
          <genius-button :button-color="row[0]" ></genius-button>
          <genius-button :button-color="row[1]" ></genius-button>
        </div>
      </template>
    </div>
    <div class="center">
      <h1 class="brand">
        Geniusus
      </h1>
      <score-display></score-display>
    </div>
  </div>
</template>

<script>
import GeniusButton from './components/GeniusButton'
import ScoreDisplay from './components/ScoreDisplay'
export default {
  name: 'App',
  components: {
    GeniusButton,
    ScoreDisplay
  },
  data() {
    return {
      rowsList: {'1': ['green','red'], '2': ['yellow','blue']}
    }
  }
}
</script>

<style>
  .back {
    width: 472px;
    height: 472px;
    border-radius: 100%;
    position: relative;
    text-align: center;
    margin: auto;
    background-color: #333;
    top: 10vh;
    box-shadow: 0 0 12px #222;
  }
  .genius{
    position: relative;
    top: 12px;
  }
  .row {
    margin-bottom: -4px;
  }
  .center {
    width: 180px;
    height: 180px;
    position: absolute;
    border-radius: 100%;
    top: 50%;
    left: 50%;
    margin: -102px 0 0 -102px;
    background-color: #ECE7EE;
    border: 12px solid #333;
  }
  .brand {
    color: #222;
    font-size: 2.2em;
    margin-top: 35px;
  }
</style>
