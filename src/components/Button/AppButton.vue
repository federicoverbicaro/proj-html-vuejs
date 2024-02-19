<template>
    <button type="button" class="btn rounded-5 " :class="computedClass">
        <span v-if="icon" class="icon">
            <img :src="icon" alt="icona">
        </span>
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
        buttonText: {
            type: String,
            default: 'Default Yellow Text'
        },
        
        icon: String,

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
</style>