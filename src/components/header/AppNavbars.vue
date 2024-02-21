<template>
    <nav id="navbars" class="navbar navbar-expand-lg p-4 d-flex justify-content-between ">

        <div class="container-fluid m-0 ">
            <div class="col-2 col-lg-2 ">
                <img class="" src="../../assets/img/theme_eduprime_logo.png" height="80%" width="80%" alt="logo">
            </div>

            <div class="col-10 collapse navbar-collapse justify-content-end" id="navbarSupportedContent">

                <ul class="navbar-nav gap-2 mb-2 mb-lg-0 d-flex align-items-center">

                    <li v-for="(menuItem, index) in menuItems" :key="index"
                        :class="{ 'nav-item': true, 'dropdown': menuItem.dropdown }">
                        <a v-if="!menuItem.dropdown" class="nav-link" :href="menuItem.url">{{ menuItem.text }}</a>
                        <a v-else class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                            aria-expanded="false">
                            {{ menuItem.text }}
                        </a>

                        <ul  v-if="menuItem.dropdown" class="dropdown-menu">

                            <li  v-for="(subItem, subIndex) in menuItem.submenu" :key="subIndex"><a class="dropdown-item" id="textDropdown"
                                    :href="subItem.url">{{ subItem.text }}</a>
                            </li>
                        </ul>

                    </li>

                </ul>
                <button class="text-uppercase">view courses</button>
            </div>

        </div>

    </nav>
</template>

<script>




export default {
    name: 'AppNavbars',

    props: {
        menuItems: {
            type: Array,
            required: true
        },

        data() {
            return {

            };
        },
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';


nav {
    background-color: $redBg2;

    img {
        max-width: 200px;
    }

    #navbarSupportedContent>ul {
        li>a {

            text-transform: capitalize;
            color: $whiteText;

            &:hover {
                color: $yellowText;
            }
        }


        #textDropdown{
                color:$blackText;
                
                &:hover{
                    color: $yellowText;
                }

        }
    }

    button {
        background-color: $yellowBg;
        color: $whiteText;
        border: none;
        padding: 10px;
        border-radius: 30px;

        &:hover {
            background-color: $whiteBg;
            color: $redText;
        }
    }
}
</style>