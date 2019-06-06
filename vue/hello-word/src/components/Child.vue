<template>
    <button @click="handleClick">{{msg}}</button>
</template>


<script>
export default {
    props: {
        msg: {
            type: String,
            required: true,
        }
    },
    methods: {
        handleClick() {
            // console.log(123);
            this.$emit('msgFun', 'testdata');//触发父组件传递的方法msgFun,第二个参数是方法传的值
        }
    },
}
</script>


<style>



</style>
