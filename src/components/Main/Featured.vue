<template>
    <section class="fluid-container" id="featured">
        <div class="row">
            <div class="col-9 mx-auto text-center d-flex mt-5 pt-3">
                <div class="line m-4"></div>
                <div>
                    <h1>Featured Products</h1>
                </div>
                <div class="line m-4"></div>
            </div>
            <div class="col-9 mx-auto text-center">
                <p>Must have products from pur top sellers</p>
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name: "Featured",
    data(){
        return{
            features: [
                {btn: "men"},
                {btn: "women"},
                {btn: "accessories"}
            ],
            products: [
                {
                    name: "black leather jacket",
                    feature: "men, jackets, jeans",
                    oldPrice: 235,
                    newPrice: 200
                },
                {
                    name: "black leather suit",
                    feature: "men, jackets",
                    newPrice: 176
                },
                {
                    name: "blue jacket & stripe tee",
                    feature: "men, jackets, suits",
                    newPrice: 580
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
        width: 300px;
        background-color: $dark-color;
    }
    p{
        color: $dark-color;
    }
}


</style>