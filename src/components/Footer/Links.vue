<template>
  <div class="fluid-container">

  </div>
</template>

<script>
export default {
    name: "Links",
    data() {
        return{
            contact: [
                {
                    street: "1234 North Main Street",
                    city: "New York, NY 5555",
                    phone: "254.355.46.56",
                    email: "info@company.com",
                    web: "Theme-Fusion.com"
                }
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