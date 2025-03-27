<template>
 
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <!-- Home Component -->
  <HomePage />

  <!-- Dashboard Component -->
  <UserDashboard />

  <!-- Profile Component -->
  <ProfileView />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/Home.vue';
import UserDashboard from './components/Dashboard.vue';
import ProfileView from './components/Profile.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    HomePage,
    UserDashboard,
    ProfileView
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
