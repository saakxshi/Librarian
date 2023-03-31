<template>
<div>
    <h1>{{id!= 0? "Edit Book" : "Add Book"}}</h1>
    <v-form>
        <v-text-field label="Title" v-model="book.title"></v-text-field>
        <v-textarea label="Description" v-model="book.description"></v-textarea>
    </v-form>

</div>
</template>

<script>
import booksList from '@/data/books.json'
export default {
    
    data() {
        return {
            id: 0,
            book: {}
        }
    },
    mounted() {
        this.id = this.$route.params.id;
        this.book= booksList.find(rec => rec._id == this.id)
    },
}
</script>

<style lang="scss" scoped>

</style>
