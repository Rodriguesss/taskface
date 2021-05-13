<template>
  <div id="app">
    <component :is="componente" :name="name" @changedPageInitial="changeComponent" @changedIntro="changeIntro"></component>
  </div>
</template>

<script>
import InputInitial from './components/InputInitial.vue'
import PageInit from '@/components/PageInit.vue'
import Intro from '@/components/Intro.vue'

export default {
  name: 'App',
  components: {
    InputInitial, PageInit, Intro
  },
  data() {
    return {
      componente: 'Intro',
      name: ''
    }
  },
  methods: {
    changeComponent(name) {
      this.componente = 'PageInit'    
      this.name = name
    },
    changeIntro() {
      setTimeout(() =>  {
        this.componente = 'InputInitial'
      }, 1000)
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Yellowtail&display=swap');

.initial {
  font-family: 'Yellowtail', cursive;
  font-size: 2.5em;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
	line-height: 1;
}

</style>
