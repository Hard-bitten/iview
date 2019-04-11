<template>
    <Cascader :data="data4" :load-data="loadData" v-model="model"></Cascader>
</template>
<script>
    export default {
        data () {
            return {
                model:['hangzhou'],
                data4: [
                    {
                        value: 'beijing',
                        label: '北京',
                        children: [],
                        loading: false
                    },
                    {
                        value: 'hangzhou',
                        label: '杭州',
                        children: [],
                        loading:false
                    }
                ]
            };
        },
        methods: {
            setValue() {
                var v = 'ca7c0fbc-728d-42e8-b111-f5f73cf9171b,a89d891b-5c50-44c0-87b4-d4f934edc921,44736384-0ede-41ba-bf7a-59c84241851a';
                var x = v.split(',');
                var x1 = x[0].toString();
                var x2 = x[1].toString();
                var x3 = x[2].toString();

                this.value1 = x;
            }
        },
        mounted () {

        }
    };
</script>
<style>

</style>