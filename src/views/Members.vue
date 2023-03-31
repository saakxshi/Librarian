<template>
    <div>
        
                <app-header title="Members"></app-header>
                <v-list>

                    <v-list-item v-for="(item, i) in member" :key="i">
                        <v-list-item-avatar tile>
                            <v-img :src="item.img"></v-img>
                        </v-list-item-avatar>

                        <v-list-item-content>
                            <v-list-item-subtitle>{{
                                item.firstName + ' ' + item.middleName + ' ' + item.lastName
                            }}</v-list-item-subtitle>
                            <v-list-item-subtitle>Member Since: {{ item._id }}yrs</v-list-item-subtitle>
                            <v-list-item-subtitle>Mobile: {{ item.mobileNo }}</v-list-item-subtitle>



                        </v-list-item-content>

                        <v-list-item-icon>
                            <div>
                                <v-menu offset-y>
                                    <template v-slot:activator="{ on, attrs }">
                                        <!-- <v-btn v-bind="attrs" v-on="on" text>
                                            <v-icon>mdi-dots-vertical</v-icon>
                                        </v-btn> -->
                                    </template>
                                    <!-- <v-list>
                                        <v-list-item>
                                            <v-list-item-title>Edit</v-list-item-title>
                                            <v-icon>mdi-pencil</v-icon>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Delete</v-list-item-title>
                                            <v-icon>mdi-delete</v-icon>

                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Issue</v-list-item-title>
                                            <v-icon>mdi-pencil</v-icon>

                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Return</v-list-item-title>
                                            <v-icon>mdi-pencil</v-icon>

                                        </v-list-item>
                                    </v-list> -->
                                </v-menu>
                                <!-- <p>Status</p> -->
                            </div>
                        </v-list-item-icon>
                    </v-list-item>
                </v-list>
           
    </div>
</template>
    
<script>
import AppHeader from '@/components/AppHeader.vue';
import MembersList from '@/data/members.json'
export default {
    data() {
        return {
            member: MembersList

        }
    },
    components: {
        AppHeader,
    },
}
</script>
    
<style lang="scss" scoped></style>