<template>
  <div id="app" class="light" @click="change">
    <div v-if="!isOpen" class="notification">
      Tab on the screen to switch the page
    </div>
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
      page: ['landing', 'cover', 'events', 'invitation', 'people'],
      pi: 0,
      isOpen: true
    }
  },
  methods: {
    change () {
      this.isOpen = true
      const range = 5
      this.pi++
      if (this.pi === range) {
        this.pi = 0
      }
    }
  },
  mounted () {
    this.isOpen = localStorage.getItem('isOpen')
    localStorage.setItem('isOpen', true)
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
}
.notification {
  position: absolute;
  width: 150px;
  top: 15px;
  right: 15px;
  height: auto !important;
  font-size: 12px;
  padding: 5px 10px;
  border-radius: 8px;
  box-shadow: 4px 4px 8px grey;
  background-color: #22224a;
  color: white;
  z-index: 10;
}
#app {
  position: relative;
  max-width: 500px;
  margin: auto;
  padding: 125px 0px;
  height: auto;
  min-height: 100%;
  overflow-x: auto;
  background-image: url('./assets/flower-2.png');
  background-repeat: no-repeat;
  background-size: cover;
  box-shadow: 2px 2px 8px grey, -2px -2px 8px white;
}
#app > div {
  height: 100%;
}

.component-fade-enter-active, .component-fade-leave-active {
  transition: transform .3s ease;
}
.component-fade-enter, .component-fade-leave-to {
  transform: rotateY(-90deg);;
}
</style>
