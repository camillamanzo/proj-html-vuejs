<template>
    <!-- jumbo section with background image and transparent buttons -->
    <section class="jumbo container-fluid">
      <div class="row">
          <div class="col-6 mx-auto text-center" id="jumbo">
                <h1 class="text-capitalize">Brand new arrivals</h1>
                <h5 class="text-capitalize">New collection from new york</h5>
                <button class="my_transparent-btn text-uppercase">view all</button>
                <button class="my_transparent-btn text-uppercase">lookbook</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

.jumbo{
    background-image: url(../../assets/images/home1_slide_three_bg_2.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 450px;
    color: $clear-color;
    #jumbo{
        padding-top: 120px;

        h1{
        font-weight: bolder;
        font-size: 65px;
        }
        h5{
            padding: 10px 0 20px;
            text-transform: uppercase;
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