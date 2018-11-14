<template>
  <span @click="emailLink(url, {subject, body})">


  <label>
    <icon name="envelope-square" :scale="scale" color="#ff4343"></icon>
    {{name}}
  </label>
    </span>
</template>

<script>
    import objectToGetParams from '../../utils/objectToGetParams';
    import 'vue-awesome/icons/envelope-square';
    import Icon from 'vue-awesome/components/Icon';
    import PopupCenter from '../../utils/PopupCenter';
    export default {
        name: 'email',
        methods: {
            emailLink(url, {subject, body}) {

                    let shareUrl =   'mailto:' +
                    objectToGetParams({
                        subject,
                        body: body || url
                    })
                PopupCenter(shareUrl, 'title', 500, 500)
            }
        },
        props: {
            name: {
                required: false,
                type: String
            },
            url: {
                type: String,
                required: true
            },
            scale: {
                required: false,
                type: String
            },
            subject: {
                required: false,
                type: String
            },
            body: {
                required: false,
                type: String
            }
        },
        components: {
            Icon
        }
    };
</script>
<style scoped>
  label {
    color: rgb(166, 29, 85);

    cursor: pointer;
    text-align: left;

    font-family: Circular, -apple-system, system-ui, Roboto, "Helvetica Neue", sans-serif;
    font-size: 16px;
    transition: 3s;
  }
  span svg{
    margin: -5px 5px 0 0;
  }
  label:hover {
    text-decoration: underline;
  }

</style>