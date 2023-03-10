<template>
        <h1>TURBOTEST</h1>
        <test/>
        <Bottom/>
        <LESTGETINTOUCH/>
        <FotterForm/>
</template>

<script>
import test from   './components/test.vue'
import Bottom from './components/Bottom.vue'
import LESTGETINTOUCH from './components/LETSGETINTOUCH.vue'
import FotterForm from './components/FotterForm.vue'
    export default {
        name: 'app',
        components: {
            test,
            Bottom,
            LESTGETINTOUCH,
            FotterForm
        }
    }
</script>

<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>