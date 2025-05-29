<script setup lang="ts">
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import PersonalInfo from './components/PersonalInfo.vue';
import Skill from './components/Skill.vue';
import Experience from './components/Experience.vue';
import Contact from './components/Contact.vue';
</script>

<template>
  <div id="app">
    <Navbar/>
    <Home />
    <PersonalInfo />
    <Skill />
    <Experience />
    <Contact />
  </div>
</template>

<style scoped>
#app {
  scroll-snap-type: y mandatory;
}
#app div{
  scroll-snap-align: start;
  scroll-margin-top: 150px;
}
</style>
