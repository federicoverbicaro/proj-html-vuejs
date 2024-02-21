<template>
    <div>
        <AppSubscribe />
    </div>

    <div>
        <AppPartners />
    </div>
    <div>
        <AppClosure />
    </div>
</template>

<script>
import AppClosure from './AppClosure.vue';
import AppPartners from './AppPartners.vue';
import AppSubscribe from './AppSubscribe.vue';


export default {
    name: 'AppFooter',
    data() {
        return {

        };
    },
    components: {
    AppSubscribe,
    AppPartners,
    AppClosure
}
}
</script>

<style lang="scss" scoped></style>