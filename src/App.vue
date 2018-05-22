<template>
  <div id="app">
    <div class="calendar-container">
      <calendar-input></calendar-input>
    </div>
  </div>
</template>

<script>
import CalendarInput from './components/calendar-input'

export default {
  name: 'App',
  components: {
    CalendarInput
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  height: 100%;
}

.calendar-container {
  position: relative;
  height: 100%;
}
</style>
