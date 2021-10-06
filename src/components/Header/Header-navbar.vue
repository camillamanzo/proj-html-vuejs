<template>
  <div class="container-fluid">
        <nav class="navbar navbar-expand-lg navbar-light bg-light col-9 mx-auto">
            <div class="container-fluid">
                <img src="../../assets/images/classic_shop_logo1x.png" alt="Avada logo">
                <div>
                    <ul class="navbar-nav mb-3">

                        <li class="nav-item dropdown" v-for="element, index in navList" :key="index">
                            <a class="nav-link active dropdown-toggle" href="#" >{{ element.item }}</a>
                            <ul class="dropdown-menu">
                                <li><a class="dropdown-item">Action</a></li>
                                <li><a class="dropdown-item">Another action</a></li>
                                <li><a class="dropdown-item">Something else here</a></li>
                            </ul>
                        </li>
                        
                        <!-- <li class="nav-item" v-for="element, index in navList" :key="index">
                            <a class="nav-link active" aria-current="page" href="#">{{ element.item }}</a>
                        </li> -->
                        <li>
                            <a class="nav-link active" aria-current="page" href="#"><i class="fas fa-search"></i></a>
                        </li>
                        
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: "Navbar",
    data() {
        return{
            navList: [
                {item: "Home"},
                {item: "Shop"},
                {item: "Products"},
                {item: "Categories"},
                {item: "News"},
                {item: "Elements"},
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

</style>