<template>
    <!-- section composed of title buttons and products -->
    <section class="container" id="featured">

        <div class="row">
            <!-- title -->
            <div class="col-9 mx-auto text-center d-flex mt-5 pt-3">
                <div class="line my-4 mx-2"></div>
                <div>
                    <h1>Featured Products</h1>
                </div>
                <div class="line my-4 mx-2"></div>
            </div>

            <!-- subtitle -->
            <div class="col-9 mx-auto text-center">
                <p>Must have products from pur top sellers</p>
            </div>
        </div>

        <!-- buttons -->
        <div class="row">
            <div class="d-flex justify-content-center">
                <div v-for="x, i in features" :key="i">
                    <button type="button">{{ x.btn }}</button>
                </div>
            </div>
        </div>

        <!-- products section with v-for -->
        <div class="row">
            <div class="product-wrapper col-3" v-for="(element, i) in products" :key="i">
                <div class="my_products-img">
                    <img :src="element.thumbs" :alt="element.name">

                    <!-- transition on hover -->
                    <div class="hover-wrapper">

                        <!-- div with info -->
                        <div class="my_d-none" >
                            <i class="fas fa-shopping-cart"></i>
                            <span> Add to cart</span>
                            <br class="p-2">
                            <i class="fas fa-list-ul ps-3"></i>
                            <span> Details</span>
                        </div>

                    </div>
                </div>

                <!-- info on product -->
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
    },
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
        &:hover{
            background-color: $clear-color;
        }
    }
    .product-wrapper{
        position: relative;
    }

    .hover-wrapper{
        transition: all 1s ease;
        width: 75%;
        height: 0px;
        background: $active-hover;
        color: $clear-color;
        position: absolute;
        bottom: 108px;
        left: 0;
        

        .my_d-none{
            margin: 150px 70px;
            display: none;
            transition: all 1.5s ease;
        }
    }

    .product-wrapper:hover .hover-wrapper{
        height: 80%;
    }

    .product-wrapper:hover .my_d-none{
        display: block;
    }
}


</style>