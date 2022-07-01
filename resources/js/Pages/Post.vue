<template>
    <div class="single-page">
        <img :src="'/storage/' + post.cover_image" :alt="post.title">
        <h1>{{ post.title }}</h1>
        <div>
            {{post.content}}
            <hr>
            <p><strong>Category</strong>: {{ post.category.name }}</p>  
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Post',
    data() {
        return {
            post: ''
        }
    },
    mounted() {
        axios.get('/api/posts/' + this.$route.params.slug)
        .then(response => {
            //console.log(response.data);
            this.post = response.data
        })
        .catch(e => {
            console.error(e);
        })
    } 
}
</script>