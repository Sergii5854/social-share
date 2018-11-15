<template>
    <div>
        <b-button @click="showModal" variant="default">
            <img alt="share" class="share" src="./../assets/share.svg">
        </b-button>
        <b-modal ref="myModalRef"
                 hide-footer
                 hide-header
                 size="sm"
                 centered
        >

            <div class="d-block   ">
                <div class="text-left">
                    <h1 class="title">Share</h1>
                    <div class="description">
                        Check out this awesome listing: Visit Microbreweries from a Colorful Bungalow in North Park - Bungalows for Rent in San Diego
                    </div>
                </div>
                <br>
                <hr>
                <div class="share-label-wrap text-left">

                    <Facebook url="https://share-links.netlify.com/"
                              name="Facebook"
                              scale="2"
                              />

                    <hr>

                    <WhatsApp
                            name="WhatsApp"
                            url="https://share-links.netlify.com/"
                            scale="2"/>

                    <hr>

                    <Email
                            name="Email"
                            title="test"
                            subject="Share Link "
                            url="https://share-links.netlify.com/"
                            scale="2"/>

                    <br>
                    <br>
                </div>
            </div>

        </b-modal>
    </div>
</template>

<script>
    import Vue from 'vue'
    import Icon from 'vue-awesome/components/Icon';
    import Facebook from './sharelinks/Facebook.vue';
    import WhatsApp from './sharelinks/Whatsapp.vue';
    import Email from './sharelinks/Email.vue';

    export default {
        components: {
            WhatsApp,
            Facebook,
            Email
        },
        methods: {
            showModal() {
                this.$refs.myModalRef.show()
            },
            hideModal() {
                this.$refs.myModalRef.hide()
            }
        }
    }
</script>

<style scoped>
    .share {
        width: 20px;
        height: 20px;
        display: block;
    }

    .title {

        color: rgb(72, 72, 72);
        display: block;
        font-family: Circular, -apple-system, system-ui, Roboto, "Helvetica Neue", sans-serif;
        font-size: 24px;
        font-weight: 800;
        height: 30px;
        letter-spacing: normal;
        line-height: 30px;
        overflow-wrap: break-word;

        text-rendering: optimizelegibility;
        text-size-adjust: 100%;
        width: 328px;
        -webkit-font-smoothing: antialiased;
        -webkit-tap-highlight-color: rgba(0, 0, 0, 0)
    }

    .description {
        color: rgb(72, 72, 72);
        display: block;
        font-family: Circular, -apple-system, system-ui, Roboto, "Helvetica Neue", sans-serif;
        font-size: 14px;
        font-weight: 400;
        height: 54px;
        letter-spacing: normal;
        line-height: 18px;
    }

    .share-label-wrap {
        text-align: left;
    }


</style>
