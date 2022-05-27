<template>
    <div v-if="post">
        <h1>{{ post.title }}</h1>
        <p>{{ post.content }}</p>
    </div>
</template>

<script>
export default {
    name: 'PostShow',
    props: ['slug'],
    data() {
        return {
            posts: null,
            baseApiUrl: 'http://localhost:8000/api/v1/posts?home',
        }
    },
    created() {
        this.getData(this.baseApiUrl + '/' + this.slug);
    },
    methods: {
        getData(url) {
            if (url) {
                Axios.get(url)
                .then(res => {
                    this.post =  res.data.response.data;
                });
            }
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
