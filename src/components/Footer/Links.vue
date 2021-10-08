<template>
    <div class="fluid-container" id="links">
        <div class="row d-flex justify-content-center">
            <div class="col-2" id="contact-info">
                <img src="../../assets/images/classic_shop_logo_footer.png" alt="avada logo" class="logo-img">
                <div v-for="x in contact" :key="x">
                    <p>{{ x }}</p>
                </div>
            </div>
            <div class="col-2" id="top-rated">
                <h6>Top rated products</h6>
                <div v-for="y in topRated" :key="y" class="d-flex justify-content-between">
                    <div>
                        <p>{{ y.name }}</p>
                        <span><i v-for="q in 5" :key="q" class="fas fa-star"></i></span>
                        <p>{{ y.price }}</p>
                    </div>
                    
                    <img :src="y.thumbs" :alt="y.name" class="thumbs">
                </div>
            </div>
            <div class="col-2" id="recent-post">
                <h6>Recent Posts</h6>
                <div v-for="r in 6" :key="r">
                    <i class="fas fa-chevron-right"></i>
                    <span>dnwjkfjkrfd dncjke jdnfj</span>
                </div>
            </div>
            <div class="col-2" id="tags">
                <h6>tags</h6>
                <div class="my_tag" v-for="el in tags" :key="el">
                    <span>{{ el }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Links",
    data() {
        return{
            contact: [
                "1234 North Main Street",
                "New York, NY 5555",
                "phone: 254.355.46.56",
                "email: info@company.com",
                "web: Theme-Fusion.com"
            ],
            topRated: [
                {
                    name: "Leather Gloves",
                    price: 45,
                    thumbs: require("../../assets/images/leather_gloves-120x156.jpg"),
                },
                {
                    name: "Black Leather Jacket",
                    oldPrice: 235,
                    price: 200,
                    thumbs: require("../../assets/images/black_elegant_leather_jacket-120x156.jpg"),
                },
                {
                    name: "Spring Printed Dress",
                    price: 47,
                    thumbs: require("../../assets/images/spring_printed_dress-120x156.jpg"),
                },
            ],

            tags: ["black", "boots", "brown", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brown", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brown", "casual", "D&G", "Fabric"]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#links{
    background-color: $footer-bg-md;

    .logo-img{
        width: 180px;
    }

    .thumbs{
        width: 50px;
        height: 100%;
    }
}

</style>