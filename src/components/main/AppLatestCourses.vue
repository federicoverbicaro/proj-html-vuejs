<template>
    <div>
        <div class="container mt-5  ">
            <h2 class="text-capitalize ">lates courses</h2>

            <div class="mt-5 d-flex  gap-4  ">

                <div id="courses" v-for="(element, index) in latestCourses" :key="index"
                    class="d-flex flex-column justify-content-center text-center gap-3 position-relative  h-50 w-50 ">

                    <div class="d-flex justify-content-center ">
                        <img :src="element.img" :alt="element.img" height="90" width="90" class="img-fluid ">
                    </div>
                    <h6> {{ element.courses }}</h6>
                    <span>{{ element.teacher }}</span>
                    <span>${{ element.prince }}</span>

                    <div id="button">
                        <AppButton red :buttonText="'View courses'"/>
                    </div>
                </div>

                

            </div>



        </div>

    </div>
</template>

<script>
import AppButton from '../Button/AppButton.vue';

export default {
    name: 'AppLatestCourses',
    data() {


        return {

            latestCourses: [
                {
                    img: '../../src/assets/img/Decisions-icon.png',
                    courses: 'Make Better Decision',
                    teacher: 'James Colins',
                    prince: '21.00'
                },
                {
                    img: '../../src/assets/img/Speaker-icon.png',
                    courses: 'How to be a speaker',
                    teacher: 'James Colins',
                    prince: 'Free'
                },
                {
                    img: '../../src/assets/img/Network-icon.png',
                    courses: 'Network Introductions',
                    teacher: 'James Colins',
                    prince: 'Free'
                },
                {
                    img: '../../src/assets/img/Brand-icon.png',
                    courses: 'Brad Management',
                    teacher: 'James Colins',
                    prince: 'Free'
                },
            ]
        }
    },
    components:{
        AppButton,
    }
}
</script>

<style lang="scss" scoped>

h2{
    font-weight: bold;
}
#courses {
    box-shadow: -4px 9px 59px -2px rgba(227, 220, 220, 1);
    -webkit-box-shadow: -4px 9px 59px -2px rgba(227, 220, 220, 1);
    -moz-box-shadow: -4px 9px 59px -2px rgba(227, 220, 220, 1);

    padding: 30px;
    
    border-radius: 5px;


    h6 {
        font-size: 20px;
        
        
    }
    img{
        aspect-ratio: 1;
    }


    #button{
        position: absolute;
        bottom: -20px;
        right: 65px;
    }
}
</style>