<template>
    <div class="home">
        <van-button type="danger">主要按钮</van-button>
        <van-list
            v-model="loading"
            :finished="finished"
            @load="onLoad"
        >
            <van-cell v-for="item in list" :key="item" :title="item" />
        </van-list>
    </div>
</template>

<script>
import {List, Button, Cell} from 'vant';

export default {
    name: 'Home',
    data(){
        return {
            list: [123],
            loading: false,
            finished: true,
        }
    },
    components:{
        [Button.name]: Button,
        [List.name]: List,
        [Cell.name]: Cell
    },
    methods:{
        onLoad(){

        }
    }
}
</script>
