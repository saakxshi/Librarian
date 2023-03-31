<template>
    <div>

                <app-header title="Issued Books"></app-header>


                <v-list>
                    <v-row>
                        <v-list-item v-for="(item, i) in issue" :key="i">
                           
                            <v-list-item-avatar size="100" tile>
                                Return Date
                                <!-- <v-img :src="item.img"></v-img> -->
                                <br>
                                {{ item.returnDate }}
                                    
                                    
                                
                            
                            </v-list-item-avatar>
                        
                            <v-list-item-content>

                                <v-list-item-subtitle>{{ item.book.title }}</v-list-item-subtitle>
                                <v-list-item-subtitle>{{ item.member.name }}</v-list-item-subtitle>
                                <v-list-item-subtitle>Issue date: {{ item.issueDate }}</v-list-item-subtitle>

                            </v-list-item-content>

                            <v-list-item-icon>
                                <div>
                                    <v-menu offset-y>

                                        <template v-slot:activator="{ on, attrs }">
                                            <v-btn v-bind="attrs" v-on="on" text>
                                                <v-icon>mdi-dots-vertical</v-icon>
                                            </v-btn>
                                        </template>
                                        <v-list>
                                            <v-list-item>
                                                <v-list-item-title>Return</v-list-item-title>
                                                <v-icon>mdi-keyboard-return</v-icon>
                                            </v-list-item>
                                            <v-list-item>
                                                <v-list-item-title>Notify</v-list-item-title>
                                                <v-icon>mdi-bell</v-icon>
                                            </v-list-item>
                                            <v-list-item>
                                                <v-list-item-title>Approve</v-list-item-title>
                                                <v-icon>mdi-check-decagram </v-icon>
                                            </v-list-item>
                                        </v-list>
                                    </v-menu>
                               
                                </div>
                            </v-list-item-icon>
                        </v-list-item>
                    </v-row>
                </v-list>
            
    </div>
</template>
    
<script>
import AppHeader from '@/components/AppHeader.vue';
import IssuesList from '@/data/issues.json'
export default {
    data() {
        return {
            issue: IssuesList

        }
    },
    components: {
        AppHeader,
    },
}
</script>
    
<style lang="scss" scoped></style>