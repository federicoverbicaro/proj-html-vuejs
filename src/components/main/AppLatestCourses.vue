<template>
    <div>
        <div class="container mt-5  ">
            <h2 class="text-capitalize ">lates courses</h2>

            <div class="mt-5 d-flex  gap-4  ">

                <div id="courses" v-for="(element, index) in latestCourses" :key="index"
                    class="d-flex flex-column justify-content-center text-center gap-3 position-relative  w-50 ">

                    <div class="d-flex justify-content-center ">
                        <img :src="element.img" :alt="element.img" height="90" width="90" class="img-fluid ">
                    </div>
                    <h6> {{ element.courses }}</h6>
                    <span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                            class="bi bi-person-fill" viewBox="0 0 16 16">
                            <path d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6" />
                        </svg>
                        Teacher: {{ element.teacher }}</span>
                    <span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                            class="bi bi-cash" viewBox="0 0 16 16">
                            <path d="M8 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4" />
                            <path
                                d="M0 4a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H1a1 1 0 0 1-1-1zm3 0a2 2 0 0 1-2 2v4a2 2 0 0 1 2 2h10a2 2 0 0 1 2-2V6a2 2 0 0 1-2-2z" />
                        </svg>
                        Prince: ${{ element.prince }}</span>

                    <div>
                        <button id="button" class="text-capitalize ">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                class="bi bi-eye" viewBox="0 0 16 16">
                                <path
                                    d="M16 8s-3-5.5-8-5.5S0 8 0 8s3 5.5 8 5.5S16 8 16 8M1.173 8a13 13 0 0 1 1.66-2.043C4.12 4.668 5.88 3.5 8 3.5s3.879 1.168 5.168 2.457A13 13 0 0 1 14.828 8q-.086.13-.195.288c-.335.48-.83 1.12-1.465 1.755C11.879 11.332 10.119 12.5 8 12.5s-3.879-1.168-5.168-2.457A13 13 0 0 1 1.172 8z" />
                                <path
                                    d="M8 5.5a2.5 2.5 0 1 0 0 5 2.5 2.5 0 0 0 0-5M4.5 8a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0" />
                            </svg>
                            View courses
                        </button>
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
    components: {
        AppButton,
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

h2 {
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

    img {
        aspect-ratio: 1;
    }


    #button {
        position: absolute;
        bottom: -20px;
        right: 78px;
        background-color: $redBg;
        color: $whiteText;
        border: none;
        padding: 10px;
        border-radius: 30px;
    }
}
</style>