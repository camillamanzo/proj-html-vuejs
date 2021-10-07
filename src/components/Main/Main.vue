<template>
  <main>
    <Jumbo />
    <Featured />
    <Collection />
  </main> 
</template>

<script>
import Jumbo from './Jumbo.vue';
import Featured from './Featured.vue'
import Collection from './Collection.vue'

export default {
    name: "Main",
    components: {
    Jumbo,
    Featured,
    Collection,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>