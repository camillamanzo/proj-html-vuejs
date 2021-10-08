<template>

    <!-- footer payements section -->
    <section id="footer-payements">
        <div class="fluid-container">

            <!-- row with copyrights -->
            <div class="row justify-content-center">
                <div class="col-7 pb-2">
                    <span class="ps-3">Copyright 2012 - 2020 |</span>
                    <span>Avada team by Theme Fusion |</span>
                    <span>All rights reserved |</span>
                    <span>Powered by WordPress</span>
                </div>
            
            <!-- row with img of cards -->
            </div>
            <div class="row justify-content-center">
                <div class="col-3"><img src="../../assets/images/payment_cards_footer.png" alt="Payement"></div>
            </div>
        </div>
    </section>
    
  

</template>

<script>
export default {
    name: "Payements",
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#footer-payements{
    padding: 50px 0;
    background-color: $footer-bg-dark;
    color: $clear-color;
}



</style>