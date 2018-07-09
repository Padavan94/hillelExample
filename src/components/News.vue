<template>
    <div class="news">
        <h1 class="news__title">News</h1>
        <div class="news__list">
            <ul v-for="(item, index) of posts" :key="item.id" v-if="index < 10 || isAllPostsShown">
                <news-single :item="item"></news-single>
            </ul>
            <button @click="tooglePostsState">{{buttonText}}</button>
        </div>
    </div>
</template>

<script>
    import axios from 'axios';
    import NewsSingle from './NewsSingle'

    export default {
        name: "news",
        components: {
            NewsSingle
        },
        data: function () {
            return {
                posts: [],
                errors: [],
                isAllPostsShown: false
            }
        },

        methods: {
          tooglePostsState() {
              this.isAllPostsShown = !this.isAllPostsShown;
          }
        },

        computed: {
            buttonText: function () {
              return this.isAllPostsShown? 'Show less' : 'Show more'
            },
        },

        mounted() {
            axios.get('https://jsonplaceholder.typicode.com/posts')
              .then(response => this.posts = response.data)
              .catch(error => this.errors.push(error))
        }
    }

</script>

<style scoped>

</style>