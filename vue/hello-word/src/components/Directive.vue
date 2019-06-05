<template>
    <!-- <div id="hook-arguments-example" v-demo:foo.a.b="message"></div> -->
    <!-- <p>Scroll down the page</p> -->
    <p v-test1:left="[testLeft]">I’ll now be offset from the left instead of the top</p>

</template>



<script>
export default {
    name: 'Directive',
    data() {
        return {
            message: 'hello!',
            testLeft: '500', //可以自定义
        }
    },
     directives: {
        // 指令名称
        dir1: {
            inserted(el) {
                // 指令中第一个参数是当前使用指令的DOM
                // console.log(el);
                // console.log(arguments);
                // 对DOM进行操作
                el.style.width = '200px';
                el.style.height = '200px';
                el.style.background = '#000';
            }
        },
        demo: {
            inserted(el, binding, vnode) {
                var s = JSON.stringify;
                el.innerHTML =
                'name: '       + s(binding.name) + '<br>' +
                'value: '      + s(binding.value) + '<br>' +
                'expression: ' + s(binding.expression) + '<br>' +
                'argument: '   + s(binding.arg) + '<br>' +
                'modifiers: '  + s(binding.modifiers) + '<br>' +
                'vnode keys: ' + Object.keys(vnode).join(', ')
            }
        },
        test1: {
            inserted(el, binding) {
                el.style.position = 'fixed';
                const s = (binding.arg == 'left' ? 'left' : 'top');
                el.style[s] = binding.value + 'px';

            }
        },
    }
}


</script>


<style>


</style>
