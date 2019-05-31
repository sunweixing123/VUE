<template>
    <div class="toList">
        <input v-model="info" type="text" />
        <button @click="addItem">添加</button>
        <ul >
            <Check v-for="(item, index) in listData" :key="index">
                <template v-slot:item="itemProps">
                    <span
                        :style="{
                            fontSize: '20px',
                            color: itemProps.checked ? 'yellow' : 'blue'
                        }"
                    >
                        {{item}}
                    </span>

                </template>

            </Check>
        </ul>
    </div>
</template>


<script>
import Check from './Check';
export default {
    components: {
        Check,
    },
    data() {
        return {
            info: '',
            listData: [],
        };
    },
    methods: {
        addItem() {
            this.listData.push(this.info);
            this.info = '';
        }
    }

}
</script>

<style>



</style>
