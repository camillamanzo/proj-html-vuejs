<template>
  <footer>
    <Subscribe />
    <Links />
    <Payements />
  </footer>
</template>

<script>
import Subscribe from './Subscribe'
import Links from './Links'
import Payements from './Payements'

export default {
  name: "Footer",
  components: {
    Subscribe,
    Links,
    Payements
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>