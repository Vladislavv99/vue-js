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
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList"

export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
            { id: 1, title: "JavaScript", body: "Опис поста" },
            { id: 2, title: "JavaScript 2", body: "Опис поста 2" },
            { id: 3, title: "JavaScript 3", body: "Опис поста 3" },
            { id: 4, title: "JavaScript 4", body: "Опис поста 4" },
            ]
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        },
    },
    
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app{
    padding: 20px;
}

</style>