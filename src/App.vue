<template>
  <div id="app">
    <calendar-test></calendar-test>
  </div>
</template>

<script>
  import calendarPt from './components/calendar'
  export default {
    name: 'app',
    data () {
      return {
        
      }
    },
    components: {
      'calendar-test': calendarPt
    }
  }
</script>

<style>
</style>
