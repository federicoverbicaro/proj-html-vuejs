<template>
    <div id="subscribe" class="mt-4 ">

        <div class="container d-flex align-items-center  ">

            <div class="col-6 d-flex justify-content-center">
                <h2>subscribe now to our newsletter!</h2>
            </div>


            <div id="serch" class="col-6 position-relative">
                <input class="w-50  " type="email" name="" id="" placeholder="Email andress...">


                <div id="icon" class="position-absolute ">
                    <span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                            class="bi bi-send-fill" viewBox="0 0 16 16">
                            <path
                                d="M15.964.686a.5.5 0 0 0-.65-.65L.767 5.855H.766l-.452.18a.5.5 0 0 0-.082.887l.41.26.001.002 4.995 3.178 3.178 4.995.002.002.26.41a.5.5 0 0 0 .886-.083zm-1.833 1.89L6.637 10.07l-.215-.338a.5.5 0 0 0-.154-.154l-.338-.215 7.494-7.494 1.178-.471z" />
                        </svg>

                    </span>
                </div>
            </div>



        </div>

    </div>
</template>

<script>
export default {
    name: 'AppSubscribe',
    data() {


        return {}
    }
}
</script>

<style lang="scss" scoped>
@import '../../styles/general.scss';

#subscribe {
    background-color: $redBg;
    padding: 25px;

    h2 {
        color: $whiteText;
        text-transform: capitalize;
    }

    input {
        border-radius: 60px;
        padding: 10px;
        border: none;

    }

    #icon {
        width: 8%;
        right: 50%;
        top: 0;
        padding: 10px;
        border-radius: 100%;
        background-color: $yellowBg;
        color: $whiteBg;
        display: flex;
        justify-content: center;
        align-items: center;
    }

}
</style>