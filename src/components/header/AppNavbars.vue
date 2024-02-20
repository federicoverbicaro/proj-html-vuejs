<template>
    <nav class="navbar navbar-expand-lg p-4 d-flex justify-content-between ">

        <div class="container-fluid m-0 ">
            <div class="col-2 col-lg-2 ">
                <img class="" src="../../assets/img/theme_eduprime_logo.png" height="80%" width="80%" alt="logo">
            </div>

            <div class="col-10 collapse navbar-collapse justify-content-end " id="navbarSupportedContent">
                <ul class="navbar-nav gap-2  mb-2 mb-lg-0 d-flex align-items-center  ">
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle text-white" href="#" role="button" data-bs-toggle="dropdown"
                            aria-expanded="false">
                            home
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Action</a></li>
                            <li><a class="dropdown-item" href="#">Another action</a></li>
                            <li>
                                <hr class="dropdown-divider">
                            </li>
                            <li><a class="dropdown-item" href="#">Something else here</a></li>
                        </ul>
                    </li>

                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                            aria-expanded="false">
                            courses
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Action</a></li>
                            <li><a class="dropdown-item" href="#">Another action</a></li>
                            <li>
                                <hr class="dropdown-divider">
                            </li>
                            <li><a class="dropdown-item" href="#">Something else here</a></li>
                        </ul>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="#">about us</a>
                    </li>


                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                            aria-expanded="false">
                            news
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Action</a></li>
                            <li><a class="dropdown-item" href="#">Another action</a></li>
                            <li>
                                <hr class="dropdown-divider">
                            </li>
                            <li><a class="dropdown-item" href="#">Something else here</a></li>
                        </ul>
                    </li>

                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                            aria-expanded="false">
                            poges
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Action</a></li>
                            <li><a class="dropdown-item" href="#">Another action</a></li>
                            <li>
                                <hr class="dropdown-divider">
                            </li>
                            <li><a class="dropdown-item" href="#">Something else here</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">contact </a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">purchase</a>
                    </li>

                    <li>
                        <button class="text-uppercase ">view courses</button>
                    </li>

                </ul>

                

            </div>
          
        </div>
        
    </nav>
</template>

<script>
import AppButton from '../Button/AppButton.vue';



export default {
    name: 'AppNavbars',

    data() {
        return {

        };
    },
    components: {
        AppButton,
    },

}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';


nav {
    background-color: $redBg2;

    img{
        max-width: 200px;
    }
   
  #navbarSupportedContent > ul {
    li > a{
        
        text-transform: capitalize;
        color: $whiteText;

        &:hover{
            color:$yellowText;
        }
    }
  }
  button{
    background-color: $yellowBg;
    color: $whiteText;
    border: none;
    padding: 10px;
    border-radius: 30px;

    &:hover{
        background-color: $whiteBg;
        color: $redText;
    }
  }
}
</style>