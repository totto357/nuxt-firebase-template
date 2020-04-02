<template lang="pug">
v-app(dark)
  h1(v-if="error.statusCode === 404") {{ pageNotFound }}
  h1(v-else) {{ otherError }}
  nuxtlink(to="/") Home page
</template>

<script lang="ts">
import Vue from "vue"
import { Component, Prop } from "nuxt-property-decorator"

@Component({})
export default class extends Vue {
  pageNotFound = "404 Not Found"
  otherError = "An error occurred"

  @Prop() error: any

  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  }
}
</script>

<style lang="sass" scoped>
h1
  font-size: 20px
</style>
