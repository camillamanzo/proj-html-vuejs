<template>
  <main>
    <Jumbo />
  </main> 
</template>

<script>
import Jumbo from './Jumbo.vue';

export default {
    name: "Main",
    components: {
    Jumbo,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>