<template>
    <div id="hook-arguments-example" v-demo:foo.a.b="message"></div>
</template>



<script>
export default {
    name: 'Directive',
    data() {
        return {
            message: 'hello!'
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
                var s = JSON.stringify
                el.innerHTML =
                'name: '       + s(binding.name) + '<br>' +
                'value: '      + s(binding.value) + '<br>' +
                'expression: ' + s(binding.expression) + '<br>' +
                'argument: '   + s(binding.arg) + '<br>' +
                'modifiers: '  + s(binding.modifiers) + '<br>' +
                'vnode keys: ' + Object.keys(vnode).join(', ')
            }
        }
    }
}


</script>


<style>


</style>
