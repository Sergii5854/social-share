<template>
  <span @click="whatsappLink(url, title)">
    <label>
    <icon name="brands/whatsapp-square" color="#34af23" :scale="scale"></icon>
      {{name}}
      </label>

  </span>
</template>

<script>
    import objectToGetParams from '../../utils/objectToGetParams';
    import 'vue-awesome/icons/brands/whatsapp-square';
    import Icon from 'vue-awesome/components/Icon';
    import PopupCenter from '../../utils/PopupCenter';

    export default {
        name: 'whatsapp',
        methods: {
            whatsappLink(url, separator, title) {
                let shareUrl = 'https://api.whatsapp.com/send' +
                    objectToGetParams({
                        text: title ? title + separator + url : url
                    });

                PopupCenter(shareUrl, 'title', 500, 500);
            }


        },
        components: {
            Icon
        },
        props: {
            name: {
                required: false,
                type: String
            },
            url: {
                required: true,
                type: String
            },
            title: {
                required: false,
                type: String
            },
            scale: {
                required: false,
                type: String
            }
        },
        data() {
            return {
                separator: ''
            };
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