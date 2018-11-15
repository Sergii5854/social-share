<template>
    <div class="hero container">
        <div class="row ">
            <div class="col-md-5 description-block text-left order-2 order-md-1">
                <br>
                <h1>Share Link </h1>
                <br>
                <small class="slogan">ENTIRE BUNGALOW IN SAN DIEGO</small>
                <br>
                <br>
                <br>
                <p class="description">Visit Microbreweries from a Colorful Bungalow in North Park</p>

            </div>
            <div class="col-md-7  order-1 order-md-2">
                <div class="img-wrap">
                    <div class="share-block">
                        <Modal/>

                    </div>
                    <img src="./../assets/room.jpg" alt="room">
                </div>
            </div>
        </div>
    </div>

</template>

<script>
    import Modal from './Modal.vue'

    export default {
        name: 'Hero',
        components: {

            Modal
        },
        props: {
            msg: String
        }
    }
</script>


<style scoped>
    .slogan {
        color: rgb(118, 118, 118);
        display: inline;
        font-family: Circular, -apple-system, system-ui, Roboto, "Helvetica Neue", sans-serif;
        font-size: 12px;
        font-weight: 800;
        height: auto;
        letter-spacing: 1px;
        line-height: 16px;
    }

    .description-block {
        background: #f5f5f5;
        height: auto;
    }

    .description {
        font-family: Circular, -apple-system, BlinkMacSystemFont, Roboto, Helvetica Neue, sans-seri;
        font-weight: normal;
        font-size: 28px;
        line-height: 34px;
        max-height: 204px;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 6;
        -webkit-box-orient: vertical;
    }

    .img-wrap {
        position: relative;
        display: block;
        width: 100%;
        height: auto;
    }
    .img-wrap img{
        display: block;
        position: relative;
        width: 100%;
        height: auto;
    }

    .share-block {
        display: block;
        position: absolute;
        top: 30px;
        right: 20px;
        z-index: 1;

    }
</style>
