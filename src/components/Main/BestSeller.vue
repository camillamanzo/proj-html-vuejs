<template>
    <!-- section composed of title and img section -->
    <div class="container" id="best-seller">
      <div class="row">
            <div class="col-9 mx-auto text-center d-flex mt-5 pt-3">
                <div class="line my-4 mx-2"></div>
                <div>
                    <h1>Best Seller</h1>
                </div>
                <div class="line my-4 mx-2"></div>
            </div>
            <div class="col-9 mx-auto text-center">
                <p>Must have products from pur top sellers</p>
            </div>
        </div>
        <div class="row d-flex justify-content-center">
            <div class="col-1 clearfix"><i class="fas fa-chevron-left fs-1 float-end"></i></div>
            <div class="col-2" v-for="x in bestSeller" :key="x">
                <img :src="x.thumbs" alt="img">
            </div>
            <div class="col-1"><i class="fas fa-chevron-right fs-1"></i></div>
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
            ]
        }
    }

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
    i{
        color: $dark-color;
        padding-top: 120px;
    }
}
</style>