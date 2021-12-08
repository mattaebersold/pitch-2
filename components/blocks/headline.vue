<!-- Spacer block -->

<template lang='pug'>

.headline.max-w-small
  h2.style-h2 {{ block.text }}

</template>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<script lang='coffee'>
export default

	props: block: Object

</script>

<!-- ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––– -->

<style lang='stylus' scoped>

.headline
  text-align center

</style>
