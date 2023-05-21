<template>
  <div class="app">
    <my-home></my-home> {{ message }}
    <button @click="changeMessage">修改App</button>
  </div>
</template>

<script>
import { computed } from 'vue'
import MyHome from './MyHome.vue'
export default {
  components: {
    MyHome
  },
  data() {
    return {
      message: "Hello App"
    }
  },
  provide() {
    return {
      name: 'why',
      age: 18,
      message: computed(() => {
        return this.message
      })
    }
  },
  methods: {

      changeMessage: function() {
        console.log(this);
        this.message = "ioo"
      }
    
  },

}
</script>

<style lang="scss" scoped></style>