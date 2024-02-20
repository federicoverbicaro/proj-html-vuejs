<template>
    <div class="bgUniverityYear  pt-5 d-flex ">
        <div class=" d-flex flex-column  ">

            <div class="text-capitalize text-white d-flex flex-column align-items-center   ">
                <img src="../../assets/img/Clock-and-Bell.png" alt="clock and bell" height="50" width="50">

                <h2 class="mt-2">university year</h2>
            </div>

            <div id="timeLine" class="p-5 d-flex justify-content-center align-items-center position-relative h-100 ">
                <img src="../../assets/img/Timeline-Item.png" alt="TimeLine" height="100%" width="80%" class="img-fluid ">

                <div id="demoClasses" class="position-absolute top-0 w-25">
                    <h4>demo classes</h4>
                    <p>In the first week, students try to accommodate with the
                        teaching style and choose their optional courses.
                    </p>
                </div>

                <div id="graduation" class="position-absolute top-0 w-25">
                    <h4>graduation day</h4>
                    <p>On the day of graduation, all students gather for the
                        ceremony and then network and party among others.
                    </p>
                </div>

                <div id="orientation" class="position-absolute bottom-0 w-25">
                    <h4>orientation</h4>
                    <p>First day of the university year, all students gather for
                        the opening ceremony and then network with others.
                    </p>
                </div>

                <div id="evaluation" class="position-absolute bottom-0 w-25">
                    <h4>evaluation</h4>
                    <p>At the end of a semester, students take a general
                        evaluation test for every subject they're learning.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppUniveristyYear',
    data() {


        return {}
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

.bgUniverityYear {
    background-color: $redBg;
    height: 700px;

    h2 {
        background-color: rgb(219, 42, 44);
    }

    #timeLine {
        margin-top: 120px;

        h4 {
            color: $whiteText;
            text-transform: capitalize;
            text-align: center;

        }

        p {
            color: $whiteText;
            font-size: 15px;
            text-align: center;
        }

        #demoClasses {
            left: 30%;
        }

        #graduation {
            right: 15%;
        }

        #orientation {
            left: 15%;
        }
        #evaluation{
            right: 30%;
        }
    }
}
</style>