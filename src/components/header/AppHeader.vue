<template>
    <AppNavbars />
    <div class="bgOnde position-relative ">
        <div id="introducion" class="text-center d-flex flex-column justify-content-center row-gap-4">
            <div class="gap-5 d-flex justify-content-center flex-column  ">
                <h1 class="text-capitalize ">key to your succes</h1>

                <p>EduPrime is the most versatile WordPress theme for educational purposes,<br>
                    showcasing universities, courses, secondary schools etc.
                </p>
            </div>

            <div class="gap-3 d-flex justify-content-center ">

                <button id="button1" class="text-capitalize ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-search"
                        viewBox="0 0 16 16">
                        <path
                            d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001q.044.06.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1 1 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0" />
                    </svg>
                    search courses
                </button>
                <button id="button2" class="text-capitalize ">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                        class="bi bi-person-fill-add" viewBox="0 0 16 16">
                        <path
                            d="M12.5 16a3.5 3.5 0 1 0 0-7 3.5 3.5 0 0 0 0 7m.5-5v1h1a.5.5 0 0 1 0 1h-1v1a.5.5 0 0 1-1 0v-1h-1a.5.5 0 0 1 0-1h1v-1a.5.5 0 0 1 1 0m-2-6a3 3 0 1 1-6 0 3 3 0 0 1 6 0" />
                        <path
                            d="M2 13c0 1 1 1 1 1h5.256A4.5 4.5 0 0 1 8 12.5a4.5 4.5 0 0 1 1.544-3.393Q8.844 9.002 8 9c-5 0-6 3-6 4" />
                    </svg>
                    apply for university
                </button>


            </div>
        </div>

        <div id="icons" class="position-absolute d-flex flex-column  ">
            <span>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart"
                    viewBox="0 0 16 16">
                    <path
                        d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5M3.102 4l1.313 7h8.17l1.313-7zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4m7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4m-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2m7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2" />
                </svg>
            </span>
            <span>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-book"
                    viewBox="0 0 16 16">
                    <path
                        d="M1 2.828c.885-.37 2.154-.769 3.388-.893 1.33-.134 2.458.063 3.112.752v9.746c-.935-.53-2.12-.603-3.213-.493-1.18.12-2.37.461-3.287.811zm7.5-.141c.654-.689 1.782-.886 3.112-.752 1.234.124 2.503.523 3.388.893v9.923c-.918-.35-2.107-.692-3.287-.81-1.094-.111-2.278-.039-3.213.492zM8 1.783C7.015.936 5.587.81 4.287.94c-1.514.153-3.042.672-3.994 1.105A.5.5 0 0 0 0 2.5v11a.5.5 0 0 0 .707.455c.882-.4 2.303-.881 3.68-1.02 1.409-.142 2.59.087 3.223.877a.5.5 0 0 0 .78 0c.633-.79 1.814-1.019 3.222-.877 1.378.139 2.8.62 3.681 1.02A.5.5 0 0 0 16 13.5v-11a.5.5 0 0 0-.293-.455c-.952-.433-2.48-.952-3.994-1.105C10.413.809 8.985.936 8 1.783" />
                </svg>
            </span>
            <span>
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-palette"
                    viewBox="0 0 16 16">
                    <path
                        d="M8 5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3m4 3a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3M5.5 7a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0m.5 6a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3" />
                    <path
                        d="M16 8c0 3.15-1.866 2.585-3.567 2.07C11.42 9.763 10.465 9.473 10 10c-.603.683-.475 1.819-.351 2.92C9.826 14.495 9.996 16 8 16a8 8 0 1 1 8-8m-8 7c.611 0 .654-.171.655-.176.078-.146.124-.464.07-1.119-.014-.168-.037-.37-.061-.591-.052-.464-.112-1.005-.118-1.462-.01-.707.083-1.61.704-2.314.369-.417.845-.578 1.272-.618.404-.038.812.026 1.16.104.343.077.702.186 1.025.284l.028.008c.346.105.658.199.953.266.653.148.904.083.991.024C14.717 9.38 15 9.161 15 8a7 7 0 1 0-7 7" />
                </svg>
            </span>

        </div>
    </div>
</template>

<script>
import AppNavbars from './AppNavbars.vue';
import AppButton from '../Button/AppButton.vue';
import yellowIcon from '../../assets/svg/magnifying-glass-solid.svg';


export default {
    name: 'AppHeader',
    data() {
        return {
            yellowIcon: yellowIcon
        };
    },
    components: {
        AppNavbars,
        AppButton
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

#introducion {
    background-image: url(../../assets/img/Wave-1.png);
    background-repeat: no-repeat;
    background-position: bottom;
    background-size: contain;
    height: 500px;
}

.bgOnde {
    background-image: linear-gradient(rgba($redBg2, 0.8), rgba($redBg2, 0.8)), url(../../assets/img/theme_slider2_bg-1.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 500px;

    h1 {
        color: $whiteText;
    }

    p {
        color: $whiteText;
    }

    #icons {
        left: 0;
        top: 40%;
        background-color: $yellowBg;
        color: $whiteText;
        padding: 10px;
        border-radius: 10px;

    }

    #button1 {
        background-color: $yellowBg;
        color: $whiteText;
        border: none;
        padding: 10px;
        border-radius: 30px;
    }

    #button2 {
        background-color: $whiteBg;
        color: $redText;
        border: none;
        padding: 10px;
        border-radius: 30px;
    }

}</style>
