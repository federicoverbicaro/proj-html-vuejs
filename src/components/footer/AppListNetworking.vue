<template>
    <ul>
        <h5 class="mb-4">networking</h5>
        <li v-for="(element, index) in networking" :key="index">
            {{ element.text }}
        </li>
    </ul>
</template>

<script>
export default {
    name: 'AppListNetworking.vue',
    data() {


        return {}
    },
    props: {
        networking: {
            type: Array,
            required: true,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

ul {
    

    h5 {
        text-transform: capitalize;
        font-size: 20px;
        font-weight: bolder;
    }
    li{
        line-height: 50px;
        font-size: 13px;
        
        cursor: pointer;

        &:hover{
            color: $yellowText;
        }
    }
}
</style>