<template>
    <!-- section composed of title and img section -->
    <div class="container" id="best-seller">

        <!-- row with title -->
        <div class="row">

            <!-- title -->
            <div class="col-9 mx-auto text-center d-flex mt-5 pt-3">
                <div class="line my-4 mx-2"></div>
                <div>
                    <h1>Best Seller</h1>
                </div>
                <div class="line my-4 mx-2"></div>
            </div>

            <!-- subtitle -->
            <div class="col-9 mx-auto text-center">
                <p>Must have products from pur top sellers</p>
            </div>

        </div>

        <!-- row with images  -->
        <div class="row d-flex justify-content-center">
            
            <!-- left arrow -->
            <div class="col-1 clearfix">
                <i class="fas fa-chevron-left fs-1 float-end my_i"></i>
            </div>

            <!-- wrapper with v-for -->
            <div class="col-2 seller-wrapper" v-for="x in bestSeller" :key="x">
                <img :src="x.thumbs" alt="img">

                <!-- transition on hover -->
                <div class="hover-wrapper">
                    <div class="my_d-none">

                        <div>
                            <h5>Modern love tee</h5>
                            <div>women t-shirts</div>
                            <div>$ 68</div>
                        </div>
                        
                        <div>
                            <i class="fas fa-shopping-cart"></i>
                            <span> Add to cart</span>
                        </div>

                        <div>
                            <i class="fas fa-list-ul"></i>
                            <span> Details</span>
                        </div>

                    </div>
                </div>
            </div>

            <!-- right arrow -->
            <div class="col-1">
                <i class="fas fa-chevron-right fs-1 my_i"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BestSeller",
    data(){
        return{
            bestSeller: [
                {thumbs: require("../../assets/images/black_elegant_leather_jacket-200x260.jpg"),},
                {thumbs: require("../../assets/images/black_leather_jacket-200x260.jpg"),},
                {thumbs: require("../../assets/images/blue_leather_jacket-200x260.jpg"),},
                {thumbs: require("../../assets/images/hipster_black_top-200x260.jpg"),},
                {thumbs: require("../../assets/images/spring_printed_dress-200x260.jpg"),},
                // {thumbs: require("../../assets/images/black_elegant_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/black_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/blue_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/hipster_black_top-200x260.jpg"),},
                // {thumbs: require("../../assets/images/spring_printed_dress-200x260.jpg"),},
                // {thumbs: require("../../assets/images/black_elegant_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/black_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/blue_leather_jacket-200x260.jpg"),},
                // {thumbs: require("../../assets/images/hipster_black_top-200x260.jpg"),},
                // {thumbs: require("../../assets/images/spring_printed_dress-200x260.jpg"),},
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#best-seller{
    h1{
        font-weight: bolder;
    }
    .line{
        height: 1px;
        width: 350px;
        background-color: $dark-color;
    }
    p{
        color: $dark-color;
    }
    .my_i{
        color: $dark-color;
        padding-top: 120px;
        &:hover{
            color: $footer-bg-light;
        }
    }
        .seller-wrapper{
        position: relative;
    }

    .hover-wrapper{
        transition: all 1s ease;
        width: 100%;
        height: 0px;
        background: $active-hover;
        color: $clear-color;
        position: absolute;
        bottom: 0px;
        left: 0;
        

        .my_d-none{
            display: none;
            transition: all 1.5s ease;
        }
    }

    .seller-wrapper:hover .hover-wrapper{
        height: 100%;
        font-size: 12px;

        h5{
            font-weight: bolder;
        }
    }

    .seller-wrapper:hover .my_d-none{
        display: block;
    }
}
</style>