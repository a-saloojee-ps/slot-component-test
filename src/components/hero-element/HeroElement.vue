<script setup>
import { computed } from 'vue'

import './hero-element.css'

const props = defineProps({
  bgImage: {
    type: String,
    required: true
  }
})

const imageBgStyle = computed(() => {
  console.log(props.bgImage)

  return {
    backgroundImage: `url(${props.bgImage})`
  }
})
</script>

<template>
  <div class="hero-element" :style="imageBgStyle">
    <div class="hero-element__content">
      <div class="hero-element__content__header">
        <slot name="text"> </slot>
      </div>
      <div class="hero-element__content__text">
        This is some supporting text to show you how cool I am. I'm so cool that I can blow your
        socks off with some simple dummy text. How cool is that?
      </div>
      <div class="hero-element__content__cta">
        <button>Click Me to Be Cool</button>
      </div>
    </div>
  </div>
</template>
