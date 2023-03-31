<template>
<div>
    
    <app-header title="Categories"></app-header>
    <v-list>
        <v-list-item v-for="(item,i) in issues" :key="i">

            <v-list-item-content>
                <v-list-item-title v-text="item.member.name"></v-list-item-title>

                <v-list-item-subtitle v-text="item.book.title"></v-list-item-subtitle>
            </v-list-item-content>

            <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                    <v-btn v-bind="attrs" v-on="on" text>
                        <v-icon>mdi-dots-vertical</v-icon>
                    </v-btn>
                </template>
                <v-list>
                    <v-list>
                        <v-list-item>
                            <v-list-item-title>Edit</v-list-item-title>
                            <v-icon>mdi-pencil</v-icon>
                        </v-list-item>
                        <v-list-item>
                            <v-list-item-title>Delete</v-list-item-title>
                            <v-icon>mdi-delete</v-icon>
                        </v-list-item>
                    </v-list>
                </v-list>
            </v-menu>
        </v-list-item>
    </v-list>


</div>
</template>

<script>
import IssuesList from '@/data/issues.json'
import AppHeader from '@/components/AppHeader.vue'
export default {
    data() {
        return {
            issues: IssuesList

        }
    },
    components: {
        AppHeader
    }

}
</script>

<style lang="scss" scoped>

</style>
