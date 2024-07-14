<script setup>
import HeroElement from './components/hero-element/HeroElement.vue'
</script>

<template>
    <HeroElement
        bg-image="https://storage.googleapis.com/pre-script-web-public/lp/l1/l1-webinar-footer.png"
    >
        <template #text> Slot-induced header! </template>
    </HeroElement>
</template>
