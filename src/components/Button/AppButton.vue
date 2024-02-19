<template>
    <button type="button" class="border-0 px-3 py-2   rounded-5 " :class="computedClass">
        <img v-if="icon" :src="icon" alt="icona" class="img-fluid icon ">
        {{ buttonText }}
    </button>
</template>

<script>

export default {
    name: 'AppButton',
    data() {
        return {}
    },
    props: {

        //button yellow
        yellow: {
            type: Boolean,
            default: false,
        },
        

        //button white 
        white: {
            type: Boolean,
            default: false,
        },
        
       

        //button red
        red: {
            type: Boolean,
            default: false,
        },
        

        buttonText: {
            type: String,
            default: 'Default Yellow Text'
        },
        
        icon: String,
       
    },

    computed: {
        computedClass() {
            return {
                'button-yellow': this.yellow,
                'button-white': this.white,
                'button-red': this.red
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

.button-yellow {
    background-color: $yellowBg;
    color: $whiteText;
}

.button-white {
    background-color: $whiteBg;
    color: $redText;
}

.button-red {
    background-color: $redBg;
    color: $whiteText;
}

.icon {
    width: 30px;
    height: 20px; 
    background-size: contain; 
}

</style>