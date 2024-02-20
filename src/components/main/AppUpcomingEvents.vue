<template>
    <div id="upcoming" class="container-fluid pt-5 ">


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
                        <span><i class="fa-solid fa-calendar-days"></i> {{ element.date }}</span>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi tenetur iste, inventore cumque
                            accusantium error, veniam </p>
                    </div>

                    <div id="button">
                        <AppButton red :buttonText="'Find More'" />
                    </div>
                </div>

            </div>

            <div class="mt-5 d-flex justify-content-center ">
                <AppButton yellow :buttonText="'View All Events'" />
            </div>

        </div>

    </div>
</template>

<script>
import AppButton from '../Button/AppButton.vue';

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
    components: { AppButton }
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
        p{
            padding: 20px;
        }


    }

}

#button {
    position: absolute;
    bottom: -20px;
    right: 130px;

}
</style>