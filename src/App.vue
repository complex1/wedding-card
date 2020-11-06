<template>
  <div id="app" class="light" @click="change">
    <div>
      <component :is="page[pi]"/>
    </div>
  </div>
</template>

<script>
import landing from './components/landing'
import cover from './components/cover'
import invitation from './components/invitation'
import events from './components/events'
export default {
  name: 'App',
  components: {
    landing,
    cover,
    invitation,
    events
  },
  data () {
    return {
      page: ['landing', 'invitation', 'cover', 'events'],
      pi: 0
    }
  },
  methods: {
    change () {
      const range = 4
      this.pi++
      if (this.pi === range) {
        this.pi = 0
      }
    }
  }
}
</script>

<style lang="scss">
.curve {
  font-family: cursive;
  line-height: 16px;
}
html {
  height: 100%;
}
body {
  height: 100%;
  background-image: url('./assets/flower-2.png');
  background-repeat: no-repeat;
  background-size: cover;
}
#app {
  padding: 125px 0px;
  height: auto;
  min-height: 100%;
}
#app > div {
  // height: calc(100% - 250px);
  height: 100%;
}
</style>
