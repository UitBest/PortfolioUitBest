<template>
    <v-container :class="mobile ? 'pa-4' : 'pa-10'" fluid>
        <v-row>
            <v-col cols="12" md="4">
                <v-sheet height="50">
                    <div class="text-h6 text-center text-primary">Contactinformatie</div>
                </v-sheet>
                <div class="text-body-1 mt-4 text-primary" :class="mobile ? 'text-center' : ''">Uit Best</div>
                <v-divider class="mb-2 mt-1"/>
                <div class="text-body-2 d-flex justify-space-between">
                    <div>
                        Adres:<br>
                        Postcode:<br>
                        Plaats:<br>
                        KVK:<br>
                    </div>
                    <div class="text-end">
                        de Dieze 35<br>
                        5684 PR<br>
                        Best<br>
                        92576176<br>
                    </div>
                </div>
            </v-col>
            <v-spacer/>
            <v-divider
                :class="mobile && 'mb-10'"
                :vertical="! mobile"
            />
            <v-spacer/>
            <v-col cols="12" md="4">
                <v-sheet height="50">
                    <div class="text-h6 text-center text-primary">Eigenaar</div>
                </v-sheet>

                <div class="text-body-1 mt-4 text-primary" :class="mobile && 'text-center'">Timo Cuijpers</div>

                <v-divider class="mb-2 mt-1"/>

                <div class="text-body-2 d-flex justify-space-between">
                    <div>
                        Tel:<br>
                        E-mail:<br>
                    </div>
                    <div class="text-end">
                        +31 6 24 19 68 43<br>
                        <span><a class="text-white text-decoration-none" href="mailto:timo@uit.best">timo@uit.best</a></span><br>
                    </div>
                </div>
            </v-col>
            <v-divider
                :class="mobile && 'mb-10'"
                :vertical="! mobile"
            />
            <v-col cols="12" md="4">
                <v-sheet height="50">
                    <div class="text-h6 text-center text-primary">Pagina's</div>
                </v-sheet>
                <div class="text-body-1 mt-4 d-flex justify-space-between text-primary"><div>Uit Best</div> <div>Portfolio's</div></div>
                <v-divider class="mb-2 mt-1"/>
                <div class="text-body-2 d-flex justify-space-between">
                    <div>
                        <a class="text-white" href="/home">Home</a><br>
                    </div>
                    <div class="text-end">
                        <span><a class="text-white" href="https://timo.uit.best/">Timo Cuijpers</a></span><br>
                    </div>
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script setup>
    import { computed } from 'vue';
    import { useDisplay } from 'vuetify';

    const display = useDisplay();
    const mobile = computed(() => display.smAndDown.value);

</script>
