<template>
  <footer>
    <Subscribe />
    <Links />
  </footer>
</template>

<script>
import Subscribe from './Subscribe'
import Links from './Links'

export default {
  name: "Footer",
  components: {
    Subscribe,
    Links,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>