<template>
  <TreeSelect v-model='model_' :tree-data='data_' :searchable='true' />
</template>

<script>
import { setInterval, setTimeout } from 'timers';
// import TreeSelect from 'vue-super-tree-select';

export default {
    // components: {TreeSelect},
    mounted(){
        setTimeout(()=>{
            this.data_ = [
                {
                    value:'早餐',label:'早餐',
                    children: [
                        {
                            title: '北方',value:'北方',label:'北方',
                            children: [
                                {value:'豆浆',label:'豆浆'},
                                {value:'油条',label:'油条'}
                            ]
                        },
                        {
                            value:'南方',label:'南方',
                            children: [
                                {value:'肠粉',label:'肠粉'},
                                {value:'虾饺',label:'虾饺'}
                            ]
                        }
                    ]
                },
                {
                    value:'午餐',label:'午餐',
                    children: [
                        {
                            value:'北方',label:'北方',
                            children: [
                                {value:'豆浆',label:'豆浆'},
                                {value:'油条',label:'油条'}
                            ]
                        },
                        {
                            title: '南方',value:'南方',label:'南方',
                            children: [
                                {value:'肠粉',label:'肠粉'},
                                {value:'虾饺',label:'虾饺'}
                            ]
                        }
                    ]
                }
            ];
            this.model_=['早餐/南方/肠粉','早餐/北方/油条'];

        },2000);
    },
    data () {
        return {
            model_: [],
            data_: []
        };
    }
};
</script>