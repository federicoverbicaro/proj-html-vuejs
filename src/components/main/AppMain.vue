<template>
    <div class="container-fluid1 ">
        <div class="container d-flex gap-4 pt-5 ">
            <div id="coursesAvailable" class="col-7">
                <img src="../../assets/img/Books-icon.png" alt="books" height="20%" width="10%">
                <h2 class="mt-3">Thousands of courses
                    for any type of student
                </h2>
                <p>At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you
                    can find a course that satisfies your needs within a click away and applies for a course
                    in a matter of minutes. EduPrime is ranked as the most versatile university in the
                    world, thanks to the number of courses it provides.</p>
                <button class="text-capitalize ">browse through courses</button>
            </div>
            <div class="col-5 pt-5 ">
                <img src="../../assets/img/Graduation-Illustration.png" alt="" height="100%" width="100%">
            </div>
        </div>

    </div>
    <div @mouseover="stopSlide" @mouseleave="slideAttivo">
        <div id="faculties" class="text-center mt-5 ">
            <h2>Faculties available at EduPrime</h2>

            <p class="mt-4">Asingle university with a load of courses, tailored
                to satisfy any student’s needs.
            </p>
        </div>

        <div class="container-fluid p-0 border-1  mt-5 mt-5">
            <div class=" px-5 ">

                <div class=" d-flex justify-content-center ">

                    <div v-for="(element, index) in faculties" :key="index" @click="changeFaculty(index)"
                        id="facultiesAvailable"
                        class="d-flex flex-column justify-content-center border border-dark-subtle p-2">
                        <div class="d-flex justify-content-center mt-3  ">

                            <img :src="element.img" alt="Faculties" height="100%" width="60%">
                        </div>
                        <div class="text-center mt-3">
                            <span>{{ element.name }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div id="bgOpttionFaculty">
            <div class="container d-flex justify-content-center  mt-5 gap-5">
                <div class="col-6 d-flex justify-content-end  p-4 ">
                    <img :src="faculties[facultiesCorrent].img2" alt="low faculty" height="60%" width="50%">
                </div>
                <div class="col-6 p-4 ">
                    <h2 class=" p-4">{{ faculties[facultiesCorrent].name }}</h2>
                    <p class="mt-4 p-4"> {{ faculties[facultiesCorrent].text }}</p>
                    <AppButton red :button-text="'Read More'" />
                </div>
            </div>

        </div>
    </div>

    <div>
        <AppUniveristyYear />
    </div>

    <div>
        <AppUpcomingEvents />
    </div>

    <div>
        <AppLatestCourses />
    </div>
    <div>
        <AppMethodStudio />
    </div>
</template>

<script>
import AppButton from '../Button/AppButton.vue';
import AppUniveristyYear from '../main/AppUniveristyYears.vue';
import AppUpcomingEvents from '../main/AppUpcomingEvents.vue';
import AppLatestCourses from '../main/AppLatestCourses.vue';
import AppMethodStudio from '../main/AppMethodStudio.vue';


export default {
    name: 'AppMain',
    data() {
        return {
            scroll: null,
            facultiesCorrent: 0,
            faculties: [
                {
                    name: 'Low faculty',
                    img: '../src/assets/img/Gavel-v2.png',
                    text: `Learning from world-leading academics and practitioners, you'll not only receive
                    an outstanding grounding in the theory of law, but you will be able to understand
                    how those principles are applied in practice through a range of student-led
                    activities and competitions.`,
                    img2: '../src/assets/img/Gavel-Illustration-e1556884768193.png'
                },
                {
                    name: 'Economy',
                    img: '../src/assets/img/Coins-tabs-v2.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident eius debitis adipisci amet excepturi modi dolor quia ut. Doloremque, porro! Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel, praesentium!',
                    img2: '../src/assets/img/Economy.png'

                },
                {
                    name: 'Medicine',
                    img: '../src/assets/img/Medicine-tabs-v2.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident eius debitis adipisci amet excepturi modi dolor quia ut. Doloremque, porro! Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel, praesentium!',
                    img2: '../src/assets/img/Medicine.png'
                },
                {
                    name: 'Computer Science',
                    img: '../src/assets/img/Computer-tabs-v2.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident eius debitis adipisci amet excepturi modi dolor quia ut. Doloremque, porro! Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel, praesentium!',
                    img2: '../src/assets/img/Computer-Science.png'
                },
                {
                    name: 'Graphic Design',
                    img: '../src/assets/img/Palette-tabs-v2.png',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Provident eius debitis adipisci amet excepturi modi dolor quia ut. Doloremque, porro! Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel, praesentium!',
                    img2: '../src/assets/img/Graphic-Design.png'

                },
            ]

        };
    },
    components: {
        AppButton,
        AppUniveristyYear,
        AppUpcomingEvents,
        AppLatestCourses,
        AppLatestCourses,
        AppMethodStudio
    },
    methods: {
        changeFaculty(index) {
            this.facultiesCorrent = index
        },

        slide() {

            if (this.facultiesCorrent === Object.keys(this.faculties).length - 1) {
                this.facultiesCorrent = 0
            } else {
                this.facultiesCorrent = this.facultiesCorrent + 1
            }
        },

        slideAttivo() {
            this.scroll = setInterval(() => {
                this.slide()
            }, 3000)

        },

        stopSlide() {
            clearInterval(this.scroll)
        },



    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

.container-fluid1 {
    background-image: url(../../assets/img/home-background.png);
    background-position: right;
    background-repeat: no-repeat;
    background-size: cover;



}

#facultiesAvailable {
    color: $redText;
    width: 150px;

    &:hover {
        background-color: $redBg;
        color: $whiteFill;

        img {
            filter: brightness(0) invert(1);
        }
    }

}

.px-5 {
    box-shadow: 1px -9px 22px 3px rgba(227, 220, 220, 1);
    -webkit-box-shadow: 1px -9px 22px 3px rgba(227, 220, 220, 1);
    -moz-box-shadow: 1px -9px 22px 3px rgba(227, 220, 220, 1);
}

#bgOpttionFaculty {
    height: 450px;
    background-image: url(../../assets/svg/svg-0.svg);
    background-repeat: no-repeat;
    background-position: bottom;
    background-size: contain;
}

button {
    background-color: $yellowBg;
    color: $whiteText;
    border: none;
    padding: 10px;
    border-radius: 30px;

    &:hover {
        background-color: $redBg2;
        color: $whiteText;
    }
}
</style>