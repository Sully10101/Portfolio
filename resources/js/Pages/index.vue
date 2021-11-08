<template>
    <v-app id="inspire">
        <v-app-bar
            app
                color="white"
            flat
        >
            <v-container class="py-0 fill-height">
                <v-avatar
                    class="mr-10"
                    color="grey darken-1"
                    size="32"
                ></v-avatar>

                <v-btn
                    v-for="link in links"
                    :key="link"
                    text
                >
                    {{ link }}
                </v-btn>

                <v-spacer></v-spacer>

                <v-responsive max-width="260">
                    <v-text-field
                        dense
                        flat
                        hide-details
                        rounded
                        solo-inverted
                    ></v-text-field>
                </v-responsive>
            </v-container>
        </v-app-bar>

        <v-main class="grey lighten-3">
            <v-container>
                <v-row>
                    <v-col cols="2">
                        <v-sheet rounded="lg">
                            <v-list color="transparent">
                                <v-list-item
                                    v-for="n in 5"
                                    :key="n"
                                    link
                                >
                                    <v-list-item-content>
                                        <v-list-item-title>
                                            List Item {{ n }}
                                        </v-list-item-title>
                                    </v-list-item-content>
                                </v-list-item>

                                <v-divider class="my-2"></v-divider>

                                <v-list-item
                                    link
                                    color="grey lighten-4"
                                >
                                    <v-list-item-content>
                                        <v-list-item-title>
                                            Refresh
                                        </v-list-item-title>
                                    </v-list-item-content>
                                </v-list-item>
                            </v-list>
                        </v-sheet>
                    </v-col>
                    <v-col>
                        <v-sheet
                            min-height="70vh"
                            rounded="lg"
                        >
                            <v-card
                                class="mx-auto"
                                max-width="344"
                                outlined

                            >
                                <v-list-item three-line>
                                    <v-list-item-content>
                                        <div class="text-overline mb-4">
                                            OVERLINE
                                        </div>
                                        <v-list-item-title class="text-h5 mb-1">
                                            Tariq is el-mucho gei
                                        </v-list-item-title>
                                        <v-list-item-subtitle>Geiiiiiiiiiiiiiiiiiiiiiiiii</v-list-item-subtitle>
                                    </v-list-item-content>

                                    <v-list-item-avatar
                                        tile
                                        size="80"
                                        color="pink"
                                    ></v-list-item-avatar>
                                </v-list-item>

                                <v-card-actions>
                                    <v-btn
                                        outlined
                                        rounded
                                        text
                                    >
                                        Button
                                    </v-btn>
                                </v-card-actions>
                            </v-card>
                            <!--  -->
                        </v-sheet>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
    </v-app>
</template>

<script>
export default {
    data: () => ({
        links: [
            'Home',
            'Projects',
            'Profile',
            "To-do's",
        ],
    }),
}
</script>
