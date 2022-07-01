<template>
    <div class="single-page d-flex flex-column align-items-center py-5">
        <img width="600" :src="'/storage/' + post.cover_image" :alt="post.title">
        <h1>{{ post.title }}</h1>
        <div>
            {{post.content}}
            <hr>
            <p><strong>Category</strong>: {{ post.category.name }}</p>  
             <strong>Tags</strong>:
             <span v-for="tag in post.tags" :key="tag.id">
              <small> #{{ tag.name }}</small>                                       
             </span>
            
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
    created() {
        axios.get('/api/posts/' + this.$route.params.slug)
        .then(response => {
            //console.log(response.data);

            if(response.status_code === 404) {
                //console.log('404 page not found');
                this.$router.push({ name: 'not-found'});
            } else {
                //console.log('page found');
                this.post = response.data
            }
        })
        .catch(e => {
            console.error(e);
        })
    } 
}
</script>