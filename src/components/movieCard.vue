<template>
    <div class="one-special-card-box" >
        <div class="one-special-card-background">
            <div class="one-special-card-background-image"
                 :style="{'background-image':'url('+article.img_url+')'}"></div>

            <!--<img class="one-special-card-background-image" v-bind:src="article.img_url"/>-->

            <div class="one-special-card-background-mask"></div>

            <div class="one-special-card-movie-name">《{{article.subtitle}}》</div>

            <div class="one-special-card-movie-bar-bg">
                <div class="one-special-card-movie-bar-stripe"></div>
            </div>
        </div>

        <div class="one-special-card-movie-title">{{article.title}}</div>
        <div class="one-special-card-movie-desc">{{article.forward}}</div>

        <div class="one-special-card-bottom-bar">
            <div class="one-special-card-bottom-author-name">{{article.author.user_name}}</div>
            <!--<div class="one-special-card-bottom-praise-icon"><i-->
                    <!--class="one-icon"-->
                    <!--:class="{'one-icon-like': !isPraised , 'one-icon-liked': isPraised}"><sup>{{praisenum-->
                <!--| formatPraisenum}}</sup></i>-->
            <!--</div>-->
            <!--<div class="one-special-card-bottom-share-icon "><i-->
                    <!--class="one-icon one-icon-share"></i></div>-->
        </div>

    </div>


</template>

<script>
    export default {
        props: ['article']
    }
</script>

<style>
    div {
        display: block;
    }

    .one-special-card-box {
        position: relative;
        background-color: white;
        /*margin-top: 20px;*/
        margin: 20px;
        /*border: 0.5px solid #D8D8D8;*/
        border: 0.8px solid #D8D8D8;
        color: black;
        border-radius: 5px;
        flex-direction: column;
        /*height: 300px;*/

    }

    .one-special-card-background {
        position: relative;
        color: white;
    }

    .one-special-card-movie-name {
        position: absolute;
        z-index: 7;
        bottom: 25px;
        left: 10px;
        right: 10px;
        text-align: center;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        font-size: 12px;
        line-height: 14px;
    }

    .one-special-card-background-image {
        /*position: absolute;*/
        width: 100%;
        height: 220px;
        z-index: 4;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
        background-size: cover;
        color: white;
        border-radius: 2px 2px 0px 0px;
        background-repeat: no-repeat;
    }

    .one-special-card-background-mask {
        /*position: absolute;*/
        z-index: 5;
        left: 0px;
        top: 0px;
        right: 0px;
        bottom: 0px;
        border-radius: 2px 2px 0px 0px;
        background-image: -webkit-linear-gradient(top, rgba(0, 0, 0, .20) 0%, rgba(0, 0, 0, .50) 100%);
    }

    .one-special-card-movie-bar-bg {
        position: absolute;
        z-index: 7;
        bottom: 0px;
        left: 0px;
        right: 0px;
        height: 20px;
        background: rgba(51, 51, 51, .5);
        text-align: center;
        margin-top: -20px;
    }

    .one-special-card-movie-bar-stripe {
        position: absolute;
        z-index: 7;
        bottom: 5px;
        top: 5px;
        left: 0px;
        right: 0px;
        height: 10px;
        /*margin-top: 5px;*/
        background-size: 40px 20px;
        background-image: linear-gradient(90deg, transparent 75%, rgba(255, 255, 255, .5) 25%);
    }

    .one-special-card-movie-title {
        margin-top: 20px;
        margin-left: 20px;
        margin-right: 20px;
        font-size: 20px;
        line-height: 30px;
      /*//  color: black;*/
    }

    .one-special-card-movie-desc {
        margin-top: 10px;
        margin-left: 20px;
        margin-right: 20px;
        font-size: 14px;
        color: #666666;
        line-height: 28px;
    }

    .one-special-card-bottom-bar {
        position: relative;
        margin-top: 20px;
        height: 40px;
        color: #a6a6a6;
        flex-direction: row;
    }

  .one-special-card-bottom-author-name {
        position: absolute;
        left: 20px;
        top: 2px;
        font-size: 12px;
        right: 110px;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
    }

    .one-special-card-bottom-praise-icon {
        position: absolute;
        z-index: 5;
        right: 37px;
        min-width: 50px;
    }

   .one-special-card-bottom-share-icon {
        position: absolute;
        z-index: 6;
        right: 0px;
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 3px;
    }

</style>
