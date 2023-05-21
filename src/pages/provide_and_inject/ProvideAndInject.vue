<template>
  <div>
    ProvideAndInject:aaaaa {{ name }} {{ age }} {{ message }}
  </div>
</template>

<script>
  export default {
    inject: ["name", "age", "message"]
  }
</script>

<style lang="scss" scoped>

</style>