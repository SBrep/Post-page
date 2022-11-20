<template>
    <form @submit.prevent>
        <!-- <input
            :value="post.title" 
            @input="post.title = $event.target.value"   вместо этого используется v-model, по сути v-model синтаксический сахар-->
        <my-input
            v-focus
            v-model="post.title"
            class="input"
            type="text"
            placeholder="Title"/>
        <my-input
            v-model="post.body"
            class="input"
            type="text"
            placeholder="Description"/>
        <my-button
            style="align-self: flex-end; margin-top: 15px"
            @click="createPost">Create</my-button>
    </form>
</template>

<script>

export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post)
            this.post = {
                title: '',
                body: '',
            }
        },
    },
}
</script>

<style>
form {
    display: flex;
    flex-direction: column;
}

</style>