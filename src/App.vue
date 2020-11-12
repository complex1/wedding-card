<template>
  <div id="app" class="light" @click="change">
    <div v-if="!isOpen" class="notification">
      Tab on the screen to switch the page
    </div>
    <transition name="component-fade" mode="out-in">
      <component :is="page[pi]"/>
    </transition>
    <button class="n-elm n-ele-in-0" @click="autochange = !autochange; setTimer()">
      <div v-if="!autochange" class="play"></div>
      <div v-else class="pause">||</div>
    </button>
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
      isOpen: true,
      autochange: true,
      timer: null
    }
  },
  methods: {
    goLeft () {
      if (this.pi > 0) {
        this.pi--
      }
    },
    goRight () {
      if (this.pi < 4) {
        this.pi++
      }
    },
    setTimer () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setInterval(this.change, 4000)
    },
    change () {
      this.isOpen = true
      const range = 5
      if (this.autochange) {
        this.pi++
        if (this.pi === range) {
          this.pi = 0
        }
        this.setTimer()
      }
    }
  },
  mounted () {
    this.isOpen = localStorage.getItem('isOpen')
    localStorage.setItem('isOpen', true)
    this.setTimer()
  }
}
</script>

<style lang="scss">

button {
  height: 50px;
  width: 50px;
  background-color: transparent;
  border: 0px solid;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  bottom: 50px;
  left: calc(50% - 15px);
  padding: 15px;
}

.play {
      margin-top: 3px;
    margin-left: 4px;
  width: 0px;
  height: 0px;
  border-top: 10px solid transparent;
  border-left: 20px solid #777;
  border-bottom: 10px solid transparent;
}
.pause {
  font-weight: bold;
  font-size: 24px;
  color: #777;
}

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
