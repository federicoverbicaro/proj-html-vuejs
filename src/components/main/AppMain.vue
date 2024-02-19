<template>
    <div class="container-fluid1 ">
        <div class="container d-flex gap-4 pt-5 ">
            <div class="col-7">
                <img src="../../assets/img/Books-icon.png" alt="books" height="20%" width="10%">
                <h2 class="mt-3">Thousands of courses
                    for any type of student
                </h2>
                <p>At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you
                    can find a course that satisfies your needs within a click away and applies for a course
                    in a matter of minutes. EduPrime is ranked as the most versatile university in the
                    world, thanks to the number of courses it provides.</p>
                <AppButton yellow :button-text="'browse through courses'" />
            </div>
            <div class="col-5 pt-5 ">
                <img src="../../assets/img/Graduation-Illustration.png" alt="" height="100%" width="100%">
            </div>
        </div>

    </div>
    <div class="text-center mt-5 ">
        <h2>Faculties available at EduPrime</h2>

        <p class="mt-4">Asingle university with a load of courses, tailored
            to satisfy any student’s needs.
        </p>
    </div>

    <div class="container-fluid p-0 border-1 border border-dark-subtle mt-5">
        <div class=" px-5 ">

            <div class=" d-flex justify-content-center ">

                <div v-for="(element, index) in faculties" :key="index" id="facultiesAvailable"
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
        <div v-for="(element, index ) in faculties" :key="index" class="d-flex justify-content-center container mt-5 gap-5 ">
            <div class="col-6 d-flex justify-content-end ">
                <img :src="element.img2" alt="low faculty">
            </div>
            <div class="col-6 p-4 ">
                <h2>{{ element.name }}</h2>
                <p class="mt-4"> {{ element.text }}</p>
                <button>ciao</button>
            </div>
        </div>


    </div>
</template>

<script>
import AppButton from '../Button/AppButton.vue';


export default {
    name: 'AppMain',
    data() {
        return {
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
        AppButton
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
</style>