<template>
    <div class="pt-5 container">
        <div class="pt-5">
            <img src="../../assets/img/Exam-icon.png" alt="Exam" height="50" width="50">

            <div class="mt-3 d-flex">

                <div class="col-6 mt-3  ">

                    <h4 class="w-50">The most efficient
                        examination method
                    </h4>
                    <p class="w-75 mt-4 "> EduPrime has gathered teachers from around the globe to
                        brainstorm in order to facilitate the evaluation of our students.
                        Every teacher from our university has an influence on how
                        students are evaluated at his/her subject.
                    </p>

                    <div>
                        <button class="text-capitalize p-3">discover the method</button>
                    </div>
                </div>

                <div class="col-6 d-flex justify-content-center ">
                    <img src="../../assets/img/Exam-Illustration.png" alt="Exam-Illustration" height="100%" width="80%">
                </div>

            </div>
        </div>

    </div>
    <div class="pt-5 container">



        <div class="mt-3 d-flex flex-row-reverse gap-5 ">

            <div class="col-5 mt-3">
                <div class="mb-3">
                    <img src="../../assets/img/Exam-icon-1.png" alt="Exam" height="50" width="50">
                </div>

                <h4 class="w-50">The most efficient
                    examination method
                </h4>
                <p class="w-75 mt-4 "> EduPrime has gathered teachers from around the globe to
                    brainstorm in order to facilitate the evaluation of our students.
                    Every teacher from our university has an influence on how
                    students are evaluated at his/her subject.
                </p>

                <div>
                    <button class="text-capitalize p-3">list of fees</button>
                </div>
            </div>

            <div class="col-7 d-flex justify-content-center ">
                <img src="../../assets/img/Girl-Illustration.png" alt="Girl-Illustration" height="100%" width="80%">
            </div>

        </div>

    </div>
</template>

<script>
import AppButton from '../Button/appbutton.vue';

export default {
    name: 'AppMethodStudio',
    data() {
        return {};
    },
    components: {
        AppButton,
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

button {
    background-color: $redBg;
    color: $whiteText;
    border: none;
    padding: 10px;
    border-radius: 30px;

    &:hover {
        background-color: $yellowBg;
        color: $whiteText;
    }
}
</style>