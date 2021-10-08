<template>
  <div class="fluid-container" id="subscribe">
      <div class="row d-flex justify-content-center">
          <div class="d-flex col-5">
              <div class="my_round"><i class="far fa-envelope fs-2"></i></div>
              <h3 class="m-3">Subscribe now and get special offers</h3>
          </div>
          <form class="col-4 my-3">
                <input type="text" placeholder="insert your email" id="email-btn">
                <button class="my_btn text-uppercase">send</button>
          </form>
      </div>
  </div>
</template>

<script>
export default {
    name: "Subscribe"
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

#subscribe{
    background-color: $footer-bg-light;
    color: white;
    height: 190px;
    padding-top: 70px;
    margin-top: 50px;

    .my_round{
        background-color: $footer-bg-md;
        padding: 15px;
        border-radius: 50%;

        i{
            color: $dark-color;
        }
    }
    
    #email-btn{
        padding: 5px;
        margin: 0 10px;
        padding: 5px 30px;
        border: none;
        border-radius: 50px;
    }
    .my_btn{
        background-color: $active-color;
        color: $clear-color;
        font-weight: bold;
        padding: 5px 30px;
        margin: 0 10px;
        border: none;
        border-radius: 50px;

        &:hover{
            background-color: $active-hover;
        }
    }
}
</style>