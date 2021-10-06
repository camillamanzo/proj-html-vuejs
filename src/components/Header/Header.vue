<template>
  <header>
    <Account />
    <Navbar />
  </header>
</template>

<script>
import Account from './Header-account.vue';
import Navbar from './Header-navbar.vue';

export default {
  name: 'App',
  components: {
    Account,
    Navbar,
  }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>