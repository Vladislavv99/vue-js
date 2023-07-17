<template>


    <form @submit.prevent>
        <h4>Створення поста</h4>
        <input 
            v-model="post.title"
            class="input" 
            type="text" 
            placeholder="Назва поста"
        >
        <input 
            v-model="post.body"
            class="input" 
            type="text" 
            placeholder="Опис поста"
        >
        <MyButton 
            @click="createPost"
            style="align-self: flex-end; margin-top: 15px;" 
            >Створити
        </MyButton>
    </form>
</template>

<script>
import MyButton from './UI/MyButton.vue';
    export default {
        components: { MyButton },
        data() {
        return {
            post: {
                title: "",
                body: "",
            }
        };
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit("create", this.post);
            this.post = {
                title: "",
                body: "",
            };
            this.title = "";
            this.body = "";
        }
    },
}
</script>

<style scoped>
form {
    display: flex;
    flex-direction: column;
}

.input{
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
}
</style>