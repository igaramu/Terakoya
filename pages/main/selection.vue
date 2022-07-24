<template>
  <div id="home">
      <Header/>

    <div class="wrap slide-paused" ontouchstart="">
      <div class="wrap">
        <ul class="slideshow">
          <li><SVGElement class="svg-img svg-hover" name="java"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="python"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="scala"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="typescript"></SVGElement></li>
        </ul>
        <ul class="slideshow">
          <li><SVGElement class="svg-img svg-hover" name="java"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="python"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="scala"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="typescript"></SVGElement></li>
        </ul>
        <ul class="slideshow">
          <li><SVGElement class="svg-img svg-hover" name="java"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="python"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="scala"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="typescript"></SVGElement></li>
        </ul>
        <ul class="slideshow">
          <li><SVGElement class="svg-img svg-hover" name="java"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="python"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="scala"></SVGElement></li>
          <li><SVGElement class="svg-img svg-hover" name="typescript"></SVGElement></li>
        </ul>
      </div>
    </div>

  </div>
</template>

<script lang="ts">
import Vue from 'vue';

import Header from '/components/Header.vue';
import SVGElement from '/components/svg.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {Header, SVGElement},
  data() {
    return {
    }
  }
})

</script>

<style lang="scss">
@import "style/style";

.slideshow {
  display: flex;
  animation: loop-slide 10s infinite linear 1s both;
}

@keyframes loop-slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-100%);
  }
}

.ul {
  text-align: center;
}

.svg-img{
  height: 100px;
  width: 200px;
}

.wrap {
  align-items: center;
  display: flex;
  height: 150px;
  margin: auto;
  justify-content: center;
  overflow: hidden;
  width: 700px;
}

.slide-paused:hover .slideshow {
  animation-play-state: paused;
}

.svg-hover {
  transition: all 0.2s;
}

li :hover {
  transform: translateY(-5px);
  box-shadow: 0 1px 5PX 0 #333;
  cursor: pointer;
}

</style>
