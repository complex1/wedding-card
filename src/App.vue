<template>
  <div id="app" class="light" @click="change">
    <transition name="component-fade" mode="out-in">
      <component :is="page[pi]"/>
    </transition>
  </div>
</template>

<script>
import landing from './components/landing'
import cover from './components/cover'
import invitation from './components/invitation'
import events from './components/events'
import people from './components/people'
export default {
  name: 'App',
  components: {
    landing,
    cover,
    invitation,
    events,
    people
  },
  data () {
    return {
      page: ['landing', 'invitation', 'cover', 'events', 'people'],
      pi: 0
    }
  },
  methods: {
    change () {
      const range = 5
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
  overflow-x: auto;
}
#app > div {
  height: 100%;
}

.component-fade-enter-active, .component-fade-leave-active {
  transition: opacity .3s ease;
}
.component-fade-enter, .component-fade-leave-to
/* .component-fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
