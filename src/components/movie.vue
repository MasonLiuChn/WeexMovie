<template>
    <div class="g-flex-row">
        <div class="g-flex-center" @click="test2(data.one.url)">
            <image class="card-poster" v-bind:src="data.one.img"
                   v-bind:placeholder="data.one.placeholder"></image>
            <div class="card-btn g-flayer">
                <text class="card-btn-text">{{data.one.status}}</text>
            </div>
            <div class="card-btn-bottom">
                <text class="card-btn-text">{{data.one.title}}</text>
            </div>
        </div>
        <div class="g-flex-center" @click="test2(data.two.url)">
            <image class="card-poster" v-bind:src="data.two.img"
                   v-bind:placeholder="data.one.placeholder"></image>
            <div class="card-btn g-flayer">
                <text class="card-btn-text">{{data.two.status}}</text>
            </div>
            <div class="card-btn-bottom">
                <text class="card-btn-text">{{data.two.title}}</text>
            </div>
        </div>
        <div class="g-flex-center" @click="test2(data.three.url)">
            <image class="card-poster" v-bind:src="data.three.img"
                   v-bind:placeholder="data.one.placeholder"></image>
            <div class="card-btn g-flayer">
                <text class="card-btn-text">{{data.three.status}}</text>
            </div>
            <div class="card-btn-bottom">
                <text class="card-btn-text">{{data.three.title}}</text>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .cell-item {
        height: 200px;
    }
    .title {
        font-size: 32px;
        font-weight: bold;
        color: #FF6600;
    }
    .g-flex-row {
        display: flex;
        flex-direction: row;
    }
    .g-flex-column {
        display: flex;
        flex-direction: column;
    }

    .g-flayer {
        position: absolute;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
    }

    .g-flex-center {
        flex: 1;
        justify-content: center; /*针对子view 是行内元素才起作用*/
        align-items: center; /*针对子view 是行内元素才起作用*/
        margin-bottom: 15px;
    }

    .padding {
        padding: 10px;
    }

    .g-flex-full {
        flex: 1;
    }

    .root {
        background-color: #E7E8EA;
    }

    .list {
        width: 750px;
        background-color: #EFEFEF;
    }
    .row {
        flex-direction: row;
    }

    .tab-cell {
        justify-content: stretch;
        background-color: #f51438;
    }
    .tab {
        height: 120px;
        width: 150px;
        justify-content: center;
        align-items: center;
    }
    .tab-icon {
        width: 45px;
        height: 45px;
    }
    .tab-title {
        font-size: 28px;
        color: #FFF;
        margin-top: 10px;
    }

    .banner-image {
        width: 750px;
        height: 235px;
    }

    .app-cell { background-color: #FFF; }
    .card-message {
        margin-top:10px;
        margin-bottom:10px;
        margin-right:10px;
    }
    .app-title {
        width: 180px;
        font-size: 30px;
        text-align: center;
        padding-top: 15px;
        color: #999999;
    }
    .app-icon {
        width: 140px;
        height: 140px;
        margin-left: 20px;
    }

    .card {
        width: 740px;
        margin-left: 5px;
        margin-top:5px;
        margin-bottom:0px;
        margin-right: 5px;
        background-color: #FFFFFF;
        border-radius: 0px;
        padding-right: 5px;
    }
    .card-banner {
        width: 222px;
        height: 60px;
    }
    .card-side {
        padding: 10px;
    }
    .card-poster {
        width: 230px;
        height: 300px;
    }
    .card-btn-bottom {
        background-color: #3c3f41;
        width:230px;
        height: 40px;
        margin-top: -40px;
        justify-content: center;
    }
    .card-title {
        font-size: 26px;
        color: #666666;
        margin-top: 10px;
        max-width: 400px;
        padding-bottom: 6px;
    }
    .card-line {
        align-items: center;
        padding-top: 5px;
        padding-bottom: 5px;
    }
    .card-icon {
        width: 36px;
        height: 36px;
        margin-right: 8px;
    }
    .card-subtitle {
        font-size: 28px;
        color: #07152a;
    }
    .card-progress {
        flex-direction: row;
        align-items: center;
        width: 100px;
        height: 30px;
        background-color: #FEC1C1;
        border-radius: 20px;
        margin-top: 10px;
        margin-bottom: 10px;
    }
    .card-progress-inner {
        position: absolute;
        height: 30px;
        left: 0;
        border-radius: 20px;
        background-color: #ff3c32;
    }
    .card-got {
        position: absolute;
        left: 8px;
        line-height: 30px;
        color: #FFFFFF;
        font-size: 22px
    }
    .card-remain {
        position: absolute;
        right: 8px;
        line-height: 30px;
        color: #FFFFFF;
        font-size: 22px;
    }
    .card-info {
        width: 400px;
        flex-direction: row;
        align-items: flex-end;
    }
    .card-price {
        font-size: 52px;
        color: #ff3c32;
        margin-bottom: -10px;
        margin-top: 10px;
        margin-right: 8px;
    }
    .card-sale-price {
        font-size: 28px;
        color: #999999;
        text-decoration: line-through;
    }
    .card-btn {
        background-color: #ff5d62;
        border-radius: 8px;
        width:200px;
        height: 40px;
        margin-top: 5px;
        margin-left: 20px;
        justify-content: center;
    }
    .card-btn-text {
        color: #FFFFFF;
        font-size: 26px;
        text-align: center;
        lines :1;
    }

    .floor {
        margin-bottom: 15px;
        background-color: #FFF;
    }
    .floor-title {
        font-size: 40px;
        text-align: center;
        padding-top: 35px;
        padding-bottom: 25px;
    }
    .floor-desc {
        lines: 2;
        color: #999;
        font-size: 30px;
        padding-left: 30px;
        padding-right: 30px;
    }
    .floor-image-box {
        flex-direction: row;
        justify-content: space-between;
        margin-top: 20px;
    }
    .floor-image {
        width: 245px;
        height: 245px;
    }
    .floor-comment {
        color: #52bfe6;
        font-size: 32px;
        text-align: right;
        padding-right: 50px;
        margin-top: 25px;
        margin-bottom: 20px;
    }
</style>

<script>

    import mixins from '../mixins'
    export default {
        mixins: [mixins],
        props: {
            data: {
                type: Object,
                required: true
            },
            'no-comment': {
                type: [String, Boolean],
                default: false
            }
        }, created () {

        },
        methods: {
            test2(url) {
                this.handle('/activity/movieDetail?url=' + url)
            }
        }
    }
</script>
