<script>
  import { Stack } from '@chriscarter90/vue-stack'
  import LayoutDefault from './layouts/LayoutDefault.vue'

  export default {
    name: 'App',

    components: {
      Stack,
      LayoutDefault,
    },

    data() {
      return {
        string: null
      }
    },

    methods: {
      boop() {
        console.log('boop', this.string)
        this.resetString()
      },

      resetString() {
        this.string = null
      }
    }
  }
</script>

<template>
  <LayoutDefault class="container">
    <Stack>
      <h1>Spotify</h1>
      <div>
        <input
          v-model="string"
          type="text"
        />
        <button @click="boop">
          Click me...
        </button>
      </div>
    </Stack>
  </LayoutDefault>
</template>

<style lang="scss" scoped>
.container {
  background-color: #fff;
  display: flex;
  margin: 0 auto;
  padding: 1rem;
  width: min(1024px, 100% - 2rem);
}
</style>
