<template>
    <!-- collection section with infos from data  -->
    <section class="container-fluid">
        <div class="row">
            <div class="col-4 wrapper" v-for="(x, i) in collections" :key="i">
                <div :style='{ backgroundImage: `url(${x.bgPath})`}' class="text-center">
                    <h1 class="text-capitalize">{{ x.coll }}</h1>
                    <h5 class="my-3">{{ x.style.toUpperCase() }}</h5>
                    <button class="my_transparent-btn text-uppercase">show more</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Collection",
    data(){
        return{
            collections: [
                {
                    bgPath: require("../../assets/images/winter_collection_bg.jpg"),
                    coll: "winter collection",
                    style: "stylish and warm"
                },
                {
                    bgPath: require("../../assets/images/spring_collection_bg.jpg"),
                    coll: "spring collection",
                    style: "bright and colorful"
                },
                {
                    bgPath: require("../../assets/images/autumn_collection_bg.jpg"),
                    coll: "autumn collection",
                    style: "rich and comfortable"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

.wrapper{
    padding: 0;
    color: $clear-color;

    div{
        height: 450px;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;

        h1{
            padding-top: 240px;
            font-weight: bolder;
        }

        .my_transparent-btn{
            background-color: $transparent-white;
            color: $clear-color;
            font-weight: bold;
            padding: 10px 20px;
            margin: 0 10px;
            border: 2px solid $clear-color;
            border-radius: 50px;
            &:hover{
                background-color: $transparent-hover;
            }
        }
    }
}

</style>