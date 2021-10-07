<template>
    <!-- section composed of title buttons and products -->
    <section class="container" id="featured">
        <!-- title section -->
        <div class="row">
            <div class="col-9 mx-auto text-center d-flex mt-5 pt-3">
                <div class="line my-4 mx-2"></div>
                <div>
                    <h1>Featured Products</h1>
                </div>
                <div class="line my-4 mx-2"></div>
            </div>
            <div class="col-9 mx-auto text-center">
                <p>Must have products from pur top sellers</p>
            </div>
        </div>
        <!-- buttons section -->
        <div class="row">
            <div class="d-flex justify-content-center">
                <div v-for="x, i in features" :key="i">
                    <button type="button">{{ x.btn }}</button>
                </div>
            </div>
        </div>
        <!-- products section with v-for from data -->
        <div class="row">
            <div class="product-wrapper col-3" v-for="(element, i) in products" :key="i">
                <div class="my_products-img">
                    <img :src="element.thumbs" :alt="element.name">
                </div>
                <div>
                    <h5>{{ element.name }}</h5>
                    <p>{{ element.feature }}</p>
                    <p v-if="element.oldPrice"> ${{ element.oldPrice }} ${{ element.newPrice }}</p>
                    <p v-else>${{ element.newPrice }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Featured",
    data(){
        return{
            // feature array returning infos for the buttons
            features: [
                {btn: "men"},
                {btn: "women"},
                {btn: "accessories"}
            ],
            // array returning infos on products
            products: [
                {
                    name: "black leather jacket",
                    thumbs: require("../../assets/images/black_elegant_leather_jacket-400x520.jpg"),
                    feature: "men, jackets, jeans",
                    oldPrice: 235,
                    newPrice: 200
                },
                {
                    name: "black leather suit",
                    thumbs: require("../../assets/images/black_leather_suit-400x520.jpg"),
                    feature: "men, jackets",
                    newPrice: 176
                },
                {
                    name: "blue jacket & stripe tee",
                    thumbs: require("../../assets/images/blue_jacket_and_white_stripe_tee-400x520.jpg"),
                    feature: "men, jackets, suits",
                    newPrice: 580
                },
                {
                    name: "modern black leather suit",
                    thumbs: require("../../assets/images/modern_black_leather_suit-400x520.jpg"),
                    feature: "men, jackets",
                    newPrice: 96
                }

            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#featured{
    height: 100vh;

    h1{
        font-weight: bolder;
    }
    .line{
        height: 1px;
        width: 280px;
        background-color: $dark-color;
    }
    p{
        color: $dark-color;
    }
    img{
        width: 70%;
    }
    button{
        display: inline-block;
        border: 1px solid $dark-color;
        width: 150px;
        padding: 10px 10px;
        margin: 40px 0;
    }
}


</style>