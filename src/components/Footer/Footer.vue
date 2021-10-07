<template>
  <footer>
    <Subscribe />
  </footer>
</template>

<script>
import Subscribe from './Subscribe'

export default {
  name: "Footer",
  components: {
    Subscribe,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>