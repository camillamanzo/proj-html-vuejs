<template>

    <!-- footer section with links -->
    <section id="links">
        <div class="container">
            <div class="row d-flex justify-content-around">

                <!-- contact info -->
                <div class="col-sm-7 col-md-5 col-lg-2 pt-2" id="contact-info">
                    <img src="../../assets/images/classic_shop_logo_footer.png" alt="avada logo" class="logo-img my-3 pb-3">
                    <div v-for="x in contact" :key="x">
                        <p class="m-1">{{ x }}</p>
                    </div>

                    <!-- social media links -->
                    <div class="pt-5">
                        <span><i class="fab fa-facebook-f"></i></span>
                        <span><i class="fab fa-twitter"></i></span>
                        <span><i class="fab fa-instagram"></i></span>
                        <span><i class="fab fa-youtube"></i></span>
                    </div>
                </div>

                <!-- top rated -->
                <div class="col-sm-7 col-md-5 col-lg-2 pt-5" id="top-rated">
                    <h6>Top rated products</h6>

                    <!-- v-for with info taken from data -->
                    <div v-for="y in topRated" :key="y" class="d-flex justify-content-between">
                        <div>
                            <p class="m-1">{{ y.name }}</p>
                            <span><i v-for="q in 5" :key="q" class="fas fa-star"></i></span>
                            <p class="m-1">$ {{ y.price }}</p>
                        </div>
                        <hr>
                        <img :src="y.thumbs" :alt="y.name" class="thumbs">
                    </div>
                </div>

                <!-- recent posr section -->
                <div class="col-sm-7 col-md-5 col-lg-2 pt-5" id="recent-post">
                    <h6>Recent Posts</h6>
                    <div v-for="r in 6" :key="r">
                        <i class="fas fa-chevron-right"></i>
                        <span> dnwjkfjkrfd dncjke jdnfj</span>
                        <hr>
                    </div>
                </div>

                <!-- tag section -->
                <div class="col-sm-7 col-md-5 col-lg-2 pt-5" id="tags">
                    <h6>tags</h6>
                    <div class="my_tag p-1 m-1" v-for="el in tags" :key="el">
                        <span>{{ el }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
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

            tags: ["black", "boots", "brown", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brownnvjdfkfhjgk", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brown", "casual"]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#links{
    background-color: $footer-bg-md;
    color: $clear-color;
    font-size: 12px;
    font-weight: bold;
    padding: 50px 0;

    .container{
        width: 85%;
    

        h6{
            text-transform: uppercase;
            font-weight: bolder;
            font-size: 12px;
            padding-bottom: 20px;
        }

        hr{
            color: $footer-bg-light;
            height: 2px;
            margin: 9px 0;
        }

        .logo-img{
            width: 180px;
        }

        .thumbs{
            width: 50px;
            height: 100%;
            margin: 2px 0;
        }

        .my_tag{
            border: 1px solid $footer-bg-light;
            display: inline-block;
        }

        #contact-info{
            i{
                font-size: 16px;
                margin: 0 5px;
            }
        }

        #top-rated{
            i{
                color: $active-color;
            }
        }
    }
}

</style>