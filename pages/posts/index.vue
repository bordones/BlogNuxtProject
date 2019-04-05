<template>
    <div class="post-page">
        <PostList :posts="loadedPosts" />
    </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
    computed : {
        loadedPosts(){
            console.log(this.$store.getters.loadedPosts);
           return this.$store.getters.loadedPosts
           //console.log($store.poststore.state.loadedPosts)
        } 
    }
}
</script>


<style scoped>
    .post-page {
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
