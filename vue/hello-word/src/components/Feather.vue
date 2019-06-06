<template>
    <Child :msg="testData" @msgFun="tranData"></Child>
</template>


<script>
import Child from './Child';
export default {
    components: {
        Child,
    },
    data() {
        return {
            testData: '点击',
        }
    },
    methods: {
        tranData(msg) {
            console.log(msg);

        }
    }
}
</script>


<style>

</style>
