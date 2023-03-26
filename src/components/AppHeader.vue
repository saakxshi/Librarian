<template>
    <div class="app-header">
        <v-row>
            <v-col cols='10'>
                <h3>{{ title }}</h3>
            </v-col>
            <v-col cols='2'>
                <div class="text-right">
                    <v-btn small>
                        <v-icon>mdi-plus</v-icon>
                    </v-btn>
                </div>
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <v-text-field solo label="Search" append-icon="mdi-magnify">
                </v-text-field>
            </v-col>
        </v-row>
    </div>
    </template>
    
    <script>
    export default {
        props: {
            title: {
                type: String
            },
        },
    }
    </script>
    
    <style lang="scss" scoped>
    .app-header {
        padding: 1rem
    }
    </style>