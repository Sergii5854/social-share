
<template>
    <div class="hero container">
        <div class="row">
            <div class="col-sm-6">
                <h1>Share Link </h1>
                <Modal />
            </div>
            <div class="col-sm-6">
                <img src="./../assets/room.jpg" alt="room">
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
