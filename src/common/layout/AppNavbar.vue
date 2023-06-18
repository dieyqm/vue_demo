<template>
    <div>
        <v-app-bar app color="#F8F9FF" flat class="app-navbar">
            <!-- <v-app-bar-nav-icon class="btn-mini-variant" @click.stop="$store.commit('layout/toggleMiniVariant')"></v-app-bar-nav-icon> color="#272848"-->
            <v-app-bar-nav-icon class="btn-mini-variant">
            </v-app-bar-nav-icon>
            <v-app-bar-nav-icon class="btn-drawer">
            </v-app-bar-nav-icon>

            <!-- <v-app-bar-nav-icon class="person" @click.stop="$store.commit('layout/toggleDrawer')"></v-app-bar-nav-icon> -->
            <v-spacer></v-spacer>
            <!-- <app-lang></app-lang> -->
            <v-tooltip bottom>
                <template v-slot:activator="{ on, attrs }">
                    <v-badge dot color="orange">
                        <v-btn outlined color="teal">
                            <v-icon color="#262745" v-bind="attrs" v-on="on">
                                mdi-bell
                            </v-icon>
                        </v-btn>
                    </v-badge>
                </template>
                <span>Pantalla completa</span>
            </v-tooltip>
            <v-tooltip bottom>
                <template v-slot:activator="{ on, attrs }">
                    <v-badge dot color="orange">
                        <v-btn icon>
                            <v-icon color="#262745" v-bind="attrs" v-on="on">
                                mdi-message-text
                            </v-icon>
                        </v-btn>
                    </v-badge>
                </template>
                <span>mdi-message-text</span>
            </v-tooltip>
            <v-tooltip bottom>
                <template v-slot:activator="{ on, attrs }">
                    <v-badge dot color="grey">
                        <v-btn icon>
                            <v-icon color="#262745" v-bind="attrs" v-on="on">
                                mdi-gift
                            </v-icon>
                        </v-btn>
                    </v-badge>
                </template>
                <span>mdi-gift</span>
            </v-tooltip>
            <div class="text-center pl-1">


            </div>
            <!-- <div class="hidden-md-and-down">
            <v-list-item two-line class="pa-0 ma-0">
                <v-list-item-content>
                    <v-list-item-title class="pa-0 ma-0"><span class="subtitle-2 ">{{ user.persona.nombres || "" }}</span></v-list-item-title>
                    <v-list-item-subtitle class="pa-0 ma-0"><span class="caption pa-0 ma-0">{{ user.usuario || "" }}</span> </v-list-item-subtitle>
                </v-list-item-content>
            </v-list-item>
        </div> -->

        </v-app-bar>

    </div>
    <!-- <v-toolbar extended>
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
            <v-toolbar-title>Title</v-toolbar-title>
            <v-text-field outlined label="Search here" append-icon="mdi-magnify"></v-text-field>

            <v-badge dot color="orange">
                <v-btn class="" outlined color="teal" dark>
                    <v-icon>mdi-bell</v-icon>
                </v-btn>
            </v-badge>
            <v-badge dot color="orange">
                <v-btn class="" outlined color="teal" dark>
                    <v-icon>mdi-message-text</v-icon>
                </v-btn>
            </v-badge>
            <v-badge dot color="grey">
                <v-btn class="" outlined color="grey" dark>
                    <v-icon>mdi-gift</v-icon>
                </v-btn>
            </v-badge>
            <v-btn class="" color="grey">
                <v-icon color="white">mdi-account</v-icon>
            </v-btn>
            <span>
                David
                <v-icon>mdi-menu-down</v-icon>
            </span>
        </v-toolbar> -->
    <!-- <v-card color="grey lighten-4" flat height="200px" tile>
            


           
            
            


        
    </v-card> -->
</template>

<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<style lang="scss" scoped></style>