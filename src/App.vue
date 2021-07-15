<template>
    <div class="app">
        <PostForm
                @create="createPost"
        />
        <PostList
                :posts="posts"
        />
    </div>
</template>

<script>
import PostForm from "./components/PostForm";
import PostList from "./components/PostList";

export default {
    components: {
        PostForm,
        PostList
    },
    data() {
        return {
            // likes: 0,
            // dislikes: 0,
            posts: [
                {id: 1, title: 'JavaScript', body: 'Описание поста'},
                {id: 2, title: 'JavaScript 2', body: 'Описание поста 2'},
                {id: 3, title: 'JavaScript 3', body: 'Описание поста 3'},
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post)
        },

        // addLike() {
        //     this.likes += 1
        // },
        // addDislike() {
        //     this.dislikes += 1
        // }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}


</style>
