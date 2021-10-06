<template>
      <div class="container-fluid">
        <nav class="navbar navbar-expand navbar-light bg-light col-9 mx-auto">
            <div class="container-fluid">
                <div>
                    <ul class="navbar-nav">
                        <li>
                            <a class="nav-link" aria-current="page" href="#"><i class="fab fa-facebook-f"></i></a>
                        </li>
                        <li>
                            <a class="nav-link" aria-current="page" href="#"><i class="fab fa-twitter"></i></a>
                        </li>
                        <li>
                            <a class="nav-link" aria-current="page" href="#"><i class="fab fa-instagram"></i></a>
                        </li>
                        <li>
                            <a class="nav-link" aria-current="page" href="#"><i class="fab fa-youtube"></i></a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul  class="navbar-nav">
                        <li class="nav-item dropdown my_nav-item">
                            <a class="nav-link dropdown-toggle">Shopping Cart</a>
                            <ul class="dropdown-menu">
                                <li>Action</li>
                                <li>Another action</li>
                                <li>Something else here</li>
                            </ul>
                        </li>
                        <li class="nav-item dropdown my_nav-item">
                            <a class="nav-link dropdown-toggle">My Account</a>
                            <ul class="dropdown-menu">
                                <li>Action</li>
                                <li>Another action</li>
                                <li>Something else here</li>
                            </ul>
                        </li>
                        <li class="nav-item dropdown my_nav-item">
                            <a class="nav-link dropdown-toggle">CART</a>
                            <ul class="dropdown-menu">
                                <li>Action</li>
                                <li>Another action</li>
                                <li>Something else here</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: "Account",
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/general.scss";

div.container-fluid{
    font-size: 12px;
}

</style>