<template>
    <div>
        <b-button @click="modalShow = !modalShow">
            Share
        </b-button>

        <b-modal v-model="modalShow">
            Hello From Modal!
            <hr>
            <label>
                <Facebook url="https://www.airbnb.com.mt/rooms/plus/20934793?"
                          scale="2"/>
                Facebook
            </label>
            <hr>
            <label>
                <WhatsApp url="https://www.airbnb.com.mt/rooms/plus/20934793?"
                          scale="2"/>
                WhatsApp
            </label>
            <hr>
            <label>
                <Email url="https://www.airbnb.com.mt/rooms/plus/20934793?"
                       scale="2"/>
                Email
            </label>
        </b-modal>
    </div>
</template>

<script>
    import Vue from 'vue'

    import {Facebook, Email, WhatsApp} from 'vue-socialmedia-share';

    export default {
        components: {
            WhatsApp,
            Facebook,
            Email
        },
        data() {
            return {

                custom: {
                    url: "https://mycustomdomain.com",
                    scale: "2"
                },

                modalShow: false
            }
        }
    }
</script>