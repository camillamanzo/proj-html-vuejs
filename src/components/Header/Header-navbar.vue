<template>
    <!-- header's bottom navbar with data access to dropdown menu -->
    <div class="container-fluid">
        <nav class="navbar navbar-expand navbar-light bg-light col-9 mx-auto">
            <div class="container-fluid">

                <!-- logo img -->
                <img src="../../assets/images/classic_shop_logo1x.png" alt="Avada logo">

                <!-- navbar with ul -->
                <div>
                    <ul class="navbar-nav mb-3" id="my_navbar-list">

                        <!-- v-for in the array of elements in data -->
                        <li class="nav-item dropdown my_nav-item" v-for="element, index in navList" :key="index">
                            <a class="nav-link dropdown-toggle">{{ element.item }}</a>
                            <ul class="dropdown-menu">
                                <li>Action</li>
                                <li>Another action</li>
                                <li>Something else here</li>
                            </ul>
                        </li>

                        <!-- button -->
                        <li><button class="my_btn text-uppercase">Shop now</button></li>

                        <!-- imput -->
                        <li><a class="nav-link" aria-current="page" href="#"><i class="fas fa-search"></i></a></li>

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
div.container-fluid{
    font-size: 12px;

    .my_navbar-list .my_nav-item:hover .nav-link{
        color: $active-color;
    };
    .my_btn{
        background-color: $active-color;
        color: $clear-color;
        font-weight: bold;
        padding: 5px 10px;
        margin: 0 10px;
        border: none;
        border-radius: 50px;
        &:hover{
            background-color: $active-hover;
        }
    }
}

    

</style>