<template lang="pug">
img.VuetifyLogo(alt="Vuetify Logo" src="/vuetify-logo.svg")
</template>

<script lang="ts">
import Vue from "vue"
import { Component } from "nuxt-property-decorator"

@Component({})
export default class extends Vue {}
</script>

<style lang="sass" scoped>
.VuetifyLogo
  height: 180px
  width: 180px
  transform: rotateY(560deg)
  animation: turn 3.5s ease-out forwards 1s

@keyframes turn
  100%
    transform: rotateY(0deg)
</style>
