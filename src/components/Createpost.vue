<template>
    <div>
        <h2>Tạo bài viết mới</h2>
        <input v-model="title" placeholder="Tiêu đề">
        <input v-model="author" placeholder="Tên tác giả">
        <textarea v-model="content" placeholder="Nội dung"></textarea>
        <button @click="submitPost">Đăng</button>
    </div>
</template>

<script setup>
    import {ref} from 'vue'

    const emit = defineEmits(['add-post'])

    const title = ref('')
    const author = ref('')
    const content = ref('')

    function submitPost(){
        if(title.value && author.value && content.value){
            const newPost= {
                title: title.value,
                author: author.value,
                content: content.value
            }
            emit('add-post',newPost)
            title.value=''
            author.value=''
            content.value=''
        }
    }
</script>
<style>
    input,textarea{
        display: block;
        width: 100%;
        margin: 10px 0;
        padding: 10px;
        border-radius: 5px;
        border: 1px solid #ddd;
    }
    button{
        padding: 10px 20px;
        background-color: #3498db;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
</style>