<template>


    <div class="post">
        <div>
            <div><strong>Назва:</strong> {{ post.title }}</div>
            <div><strong>Опис:</strong> {{ post.body }}</div>
        </div>
        <div class="post__btns">
            <MyButton>Видалити</MyButton>
        </div>
    </div> 
</template>

<script>
import MyButton from './UI/MyButton.vue';
export default {
    components: { MyButton },
    props: {
        post: {
            type: Array,
            required: true,
        }
    },
    
}
</script>

<style scoped>
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>