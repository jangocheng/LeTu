<template>
    <div class="container">
        <div class="bg">
            <image class="map-bg" src="http://img1.vued.vanthink.cn/vued606f6ce9ac598cf0c23e0653f4cd7d54.png" ></image>
        </div>
        <div class="map">
            <image class="logo" src="http://img1.vued.vanthink.cn/vuedf325648b3361db3cf5fdfc55510167f3.png"></image>
            <text class="title">WEEX-AMAP DEMOS</text>
        </div>
        <example-list :items="items"></example-list>
    </div>
</template>

<style>
    .container{
        position: relative;
        flex:1;
        background-color: #b5d6ea;
    }
    .bg{
        position:absolute;
        left:0;
        right:0;
        top:0;
        background-color: #b4d6eb;
    }
    .map-bg{
        flex: 1;
        height: 1130;
    }
    .title {
        color: #1995f9;
        font-size: 38px;
        padding: 20;
        align-items: center;
    }
    .logo-wrap{
        display: flex;
        align-items: center;
    }
    .logo{
        width: 160;
        height:160;
        margin-top: 40;
    }
    .map{
        height: 300;
        align-items: center;
    }
</style>

<script>
    import ExampleList from '../include/example-list.vue'
    export default {
        components: { ExampleList},
        data() {
            return {
                root: '初始化',
                items: [
                    {
                        name: 'pages/info-window',
                        title: '信息窗体',
                        imgsrc: 'http://img1.vued.vanthink.cn/vuedd739d1f8d17c13e85ebc72a7063f3465.png',
                        keyword: 'InfoWindow',
                        desc: '在地图上显示自定义的信息窗体'
                    },
                    {
                        name: 'pages/circle',
                        title: '设置圆形',
                        imgsrc: 'http://img1.vued.vanthink.cn/vued2cd00418adaf48c2f0c678cac4c48d9b.png',
                        keyword: 'Circle',
                        desc: '在地图上显示圆形覆盖物'
                    },
                    {
                        name: 'pages/polyline',
                        title: '设置折线',
                        imgsrc: 'http://img1.vued.vanthink.cn/vued759efae4808fd98635461c4a7d6c520c.png',
                        keyword: 'Polyline',
                        desc: '在地图上显示折线'
                    },
                    {
                        name: 'pages/polygon',
                        title: '设置多边形',
                        imgsrc: 'http://img1.vued.vanthink.cn/vuededa66db12403e0ccbba4d25865cb8eab.png',
                        keyword: 'Polygon',
                        desc: '在地图上显示多边形'
                    },
                    {
                        name: 'pages/polygon-contains-marker',
                        title: '多边形判断',
                        imgsrc: 'http://img1.vued.vanthink.cn/vuede1b5292b15e88ff6cff05c2f89f11956.png',
                        keyword: 'Polygon Contains',
                        desc: '判断多边形是否包含某个点'
                    },
                    {
                        name: 'pages/get-distance',
                        title: '计算距离',
                        imgsrc: 'http://img1.vued.vanthink.cn/vuede1b5292b15e88ff6cff05c2f89f11956.png',
                        keyword: 'Distance',
                        desc: '计算两个标记点的距离'
                    },
                    {
                        name: 'pages/pressure-test',
                        title: '压力测试',
                        imgsrc: 'http://img1.vued.vanthink.cn/vued76db1e0e8f6ee379797ffd35561aa849.png',
                        keyword: 'test',
                        desc: '使用地图进行用户的定位'
                    }]
            }
        }
    }
</script>
