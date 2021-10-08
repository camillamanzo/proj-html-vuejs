<template>
    <div class="fluid-container">
        <div class="row">
            <div class="col-2" id="contact-info">
                <img src="../../assets/images/classic_shop_logo_footer.png" alt="avada logo">
                <div v-for="x in contact" :key="x">
                    <p>{{ x }}</p>
                </div>
            </div>
            <div class="col-2" id="top-rated">
                
            </div>
            <div class="col-2" id="recent-posts">
                
            </div>
            <div class="col-2" id="tags">
                
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
            
            recentPost:[
                {el: "ffjnieo hfuer iuhriewrh"},
            ],

            tags: ["black", "boots", "brown", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brown", "casual", "D&G", "Fabric", "Flowers", "Grey","black", "boots", "brown", "casual", "D&G", "Fabric"]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>