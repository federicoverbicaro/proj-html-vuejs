<template>
    <div id="upcoming" class="container-fluid pt-5">


        <div class="d-flex flex-column  ">


            <div class="text-capitalize text-white d-flex flex-column align-items-center  ">
                <img src="../../assets/img/upcoming-events-calendar-icon.png" alt="upcoming" height="40" width="40"
                    class="img-fluid ">
                <h2 class="mt-2">upcoming events</h2>
            </div>

            <div class="d-flex gap-3 container pt-5 pb-5 ">
                <div v-for="(element, index) in dateSession" :key="index" class="position-relative ">

                    <div id="coaching" class="p-3 d-flex flex-column ">
                        <h4>coaching sessions</h4>
                        <span>
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                class="bi bi-calendar" viewBox="0 0 16 16">
                                <path
                                    d="M3.5 0a.5.5 0 0 1 .5.5V1h8V.5a.5.5 0 0 1 1 0V1h1a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V3a2 2 0 0 1 2-2h1V.5a.5.5 0 0 1 .5-.5M1 4v10a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V4z" />
                            </svg>
                            {{ element.date }}</span>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi tenetur iste, inventore cumque
                            accusantium error, veniam </p>
                    </div>

                    <div>
                        <button id="button1" class="text-capitalize">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                class="bi bi-plus-lg" viewBox="0 0 16 16">
                                <path fill-rule="evenodd"
                                    d="M8 2a.5.5 0 0 1 .5.5v5h5a.5.5 0 0 1 0 1h-5v5a.5.5 0 0 1-1 0v-5h-5a.5.5 0 0 1 0-1h5v-5A.5.5 0 0 1 8 2" />
                            </svg>
                            find more
                        </button>
                    </div>
                </div>

            </div>

            <div class="d-flex justify-content-center">
                <button id="button2" class=" text-capitalize ">view all events</button>
            </div>

        </div>

    </div>
</template>

<script>

import AppButton from '../Button/appbutton.vue';
export default {
    name: 'AppUpcomingEvents',
    data() {
        return {
            dateSession: [
                {
                    date: '20 May 21:30 PM'
                },
                {
                    date: '24 Mar 18:00 PM'
                },
                {
                    date: '12 Feb 13:30 PM'
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

#upcoming {
    background-color: $redBg;
    height: 800px;
    background-image: url(../../assets/img/Wave-1.png);
    background-repeat: no-repeat;
    background-position: bottom;
    background-size: contain;

    h2 {
        color: $whiteText;
        text-align: center;
        text-transform: capitalize;

    }

    #coaching {
        background-color: $whiteBg;
        text-align: center;
        border-radius: 20px;
        box-shadow: -4px 9px 59px -2px rgb(0, 0, 0);
        -webkit-box-shadow: -4px 9px 59px -2px rgb(4, 3, 3);
        -moz-box-shadow: -4px 9px 59px -2px rgb(0, 0, 0);


        h4 {
            text-transform: capitalize;
            font-weight: 900;
            margin-top: 20px;

        }

        p {
            padding: 20px;
        }


    }

}

#button1 {
    background-color: $redBg;
    color: $whiteBg;
    position: absolute;
    bottom: -20px;
    right: 36%;
    border: none;
    padding: 10px;
    border-radius: 30px;
}

#button2 {
    background-color: $yellowBg;
    color: $whiteText;
    border: none;
    padding: 10px;
    border-radius: 30px;
    margin-top: 30px;

    &:hover {
        background-color: $redBg2;
        color: $whiteText;
    }
}
</style>