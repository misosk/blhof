<template>
  <div>
    <a>
      <img id="beat" src="https://fontmeme.com/permalink/230221/a0b142652688234f9ba0343f3aa8b419.png" alt="beat-saber-font"> <img id="saber" src="https://fontmeme.com/permalink/230221/493773658a26b4d3a0f649f207cd9c76.png" alt="beat-saber-font" border="0">
      <img id="hof" src="https://fontmeme.com/permalink/230221/53aea9c0ff70254774d6d07d51196203.png" alt="beat-saber-font">
    </a>
  </div>
</template>

<script>
import * as url from 'url'

export default {
  name: 'IndexPage',
  computed: {
    url () {
      return url
    }
  }
}
</script>
<style>
  #beat {
    position: absolute;
    top: 349px;
    width: 277px;
    height: 124px;
    left: 678px;
    background-color: transparent;
    object-fit: none;
    object-position: center top;
  }

  #saber {
    position: absolute;
    right: 650px;
    top: 350px;
    width: 329px;
    height: 123px;
    background: transparent;
    object-fit: none;
    object-position: center;
  }

  #hof {
    position: absolute;
    top: 421px;
    right: 659px;
    width: 603px;
    height: 119px;
    background-color: transparent;
    object-fit: none;
    object-position: center;
  }
</style>
