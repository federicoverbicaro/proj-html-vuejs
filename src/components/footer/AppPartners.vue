<template>
    
        <div id="partners" class="container mt-4 mb-5">
            <div class="text-center d-flex align-items-center  flex-column ">

                <h2 class="text-capitalize ">partners</h2>

                <p class="w-50 pt-3  ">Leverage agile frameworks to provide a robust synopsis for high level
                    overviews. Iterative approaches to corporate strategy.
                </p>

            </div>

            <div class="d-flex gap-4 justify-content-center pt-5">
                <div v-for="(element, index) in partners" :key="index">
                    <img :src="element.img" alt="" height="40">
                </div>
            </div>



        </div>
        <div id="bgPartners"></div>
    
</template>

<script>
export default {
    name: 'AppPartners',
    data() {
        return {
            partners: [
                {
                    img: '../../src/assets/img/partner-2.png'
                },
                {
                    img: '../../src/assets/img/partner-3.png'
                },
                {
                    img: '../../src/assets/img/partner-4.png'
                },
                {
                    img: '../../src/assets/img/partner-5.png'
                },
                {
                    img: '../../src/assets/img/partner-6.png'
                },
                {
                    img: '../../src/assets/img/partner-8.png'
                },
                {
                    img: '../../src/assets/img/partner-1.png'
                },
                {
                    img: '../../src/assets/img/partner-7.png'
                },

            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';
#bgPartners{
    
    background-image: url(../../assets/img/background-wave3.png);
    background-color: $whiteLightBg2;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    height: 190px;
}

img {
    opacity: 0.4;
    cursor: pointer;

    &:hover{
        opacity: 1;
        color: $blackText2;
    }
}
</style>