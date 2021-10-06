<template>
  <main>
    <Jumbo />
    <Featured />
  </main> 
</template>

<script>
import Jumbo from './Jumbo.vue';
import Featured from './Featured.vue'

export default {
    name: "Main",
    components: {
    Jumbo,
    Featured,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>