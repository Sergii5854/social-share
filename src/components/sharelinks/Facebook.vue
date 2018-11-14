<template>
  <span @click="facebookLink(url)">
    <label>
      <icon name="brands/facebook" color="#3B5998" :scale="scale"></icon>
      {{name}}
    </label>
  </span>
</template>

<script>
    import objectToGetParams from '../../utils/objectToGetParams';
    import PopupCenter from '../../utils/PopupCenter';
    import 'vue-awesome/icons/brands/facebook';
    import Icon from 'vue-awesome/components/Icon';

    export default {
        name: 'facebook',
        components: {
            Icon
        },
        methods: {
            facebookLink(url) {
                let shareUrl = `https://www.facebook.com/sharer/sharer.php` +
                    objectToGetParams({
                        u: url
                    });
//            window.open(shareUrl, '_self')


                PopupCenter(shareUrl, 'title', 500, 500)

            }
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
            scale: {
                required: false,
                type: String
            }
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
