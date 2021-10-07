<template>
  <main>
    <Jumbo />
    <Featured />
    <Collection />
    <BestSeller />
  </main> 
</template>

<script>
import Jumbo from './Jumbo';
import Featured from './Featured';
import Collection from './Collection';
import BestSeller from './BestSeller';

export default {
    name: "Main",
    components: {
    Jumbo,
    Featured,
    Collection,
    BestSeller,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>