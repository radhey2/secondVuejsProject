<template>
  <div id="app">
  <span v-for="option in options" :key="option">
    <input v-model="checkedNames" :id="option.value" :value="option.value" type="checkbox">
    <label for="option.value">  {{option.value}}</label>
  </span>

  <br>
  <span>Checked names: {{ checkedNames }}</span>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      checkedNames: [],
      options: [
        { value: 'John' },
        { value: 'Paul' },
        { value: 'George' },
        { value: 'Ringo' }
      ]
    }
  }
}
</script>
