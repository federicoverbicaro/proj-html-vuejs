<template>
    <AppNavbars />
<div class="bgOnde">
    <div id="introducion" class="text-center d-flex flex-column justify-content-center row-gap-4">
        <div class="gap-5 d-flex justify-content-center flex-column  ">
            <h1 class="text-capitalize ">key to your succes</h1>

            <p>EduPrime is the most versatile WordPress theme for educational purposes,<br>
                showcasing universities, courses, secondary schools etc.
            </p>
        </div>

        <div class="gap-3 d-flex justify-content-center ">

            <AppButton yellow buttonText="search courses" :icon="yellowIcon" />

            <AppButton white buttonText="Apply for university" />
        </div>
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
#introducion{
    background-image: url(../../assets/img/Wave-1.png);
    background-repeat: no-repeat;
    background-position: bottom;
    height: 500px;
}

.bgOnde{
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

}
</style>
