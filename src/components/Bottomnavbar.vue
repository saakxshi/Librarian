<template>
<v-bottom-navigation app>
    <v-btn value="recent" @click="$router.push('/books')">
        <span>Books</span>

        <v-icon>mdi-bookshelf</v-icon>
    </v-btn>

    <v-btn value="favorites" @click="$router.push('/authors')">
        <span>Authors</span>

        <v-icon>mdi-badge-account</v-icon>
    </v-btn>

    <v-btn value="nearby" @click="$router.push('/')">
        <span>Members</span>

        <v-icon>mdi-account</v-icon>
    </v-btn>
</v-bottom-navigation>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

</style>
