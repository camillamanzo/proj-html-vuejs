<template>
  <section class="container-fluid">
        <div class="row">
            <div class="col-4 wrapper" v-for="(x, i) in collections" :key="i">
                <div :style='{ backgroundImage: `url(${x.bgPath})`}'>
                    <h1>{{ x.coll }}</h1>
                    <h4>{{ x.style }}</h4>
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

    div{
        height: 450px;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }
}

</style>