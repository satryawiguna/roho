<template>
    <div class="custom-container" v-if="!fullSize">
        <div class="main">
            <div class="mainbar__widget">
                <v-btn
                    elevation="2"
                    outlined
                    x-small>
                    <i class="fa fa-chevron-left"></i>
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Back to Feed
                </v-btn>
                <h1>
                    Title From Feed
                </h1>
                <div class="left">
                    <v-btn
                        elevation="2"
                        depressed
                        x-small>
                            Filter
                            <i class="fa fa-chevron-down"></i>
                    </v-btn>
                    <v-btn
                        elevation="2"
                        depressed
                        x-small>
                        Sort
                        <i class="fa fa-chevron-down"></i>
                    </v-btn>
                </div>
            </div>
            <div class="list-products">
                <v-card
                    elevation="2"
                    class="card"
                    v-for="product in products"
                    :key="product"
                >
                    <v-img
                        width="100%"
                        src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                    ></v-img>

                    <v-card-title class="card-title">LOREM IPSUM DOLOR SIT AMET</v-card-title>

                    <v-card-text class="card-text">
                        Lorem ipsum dolor set amet<br />
                        <span class="price">$1000</span>&nbsp;<span class="discount">$500</span>
                    </v-card-text>

                    <v-card-actions class="card-action">
                        <a href="#">Add to 3D Studio</a>
                        <a href="#" class="add-to-cart">Add to Cart</a>
                    </v-card-actions>
                </v-card>
            </div>
        </div>
        <aside class="sidebar">
            <div class="sidebar__widget"
                 :style="{'background-image':'url(https://nirvanaadikarya.id/wp-content/uploads/2020/06/Konsultan-Interior-Jakarta-Profesional-dan-Sangat-Berpengalaman.jpg)', 'background-size': 'cover', 'background-position': 'bottom'}">
                <v-btn
                    v-model="fullSize"
                    @click="toggleFullSize()"
                    elevation="2"
                    outlined
                    small
                    style="background-color: #fff;">
                    <i class="fa fa-chevron-left"></i>
                </v-btn>
                <div style="margin-left: auto; padding-right: 20px;">
                    <v-btn
                        elevation="2"
                        outlined
                        small
                        style="background-color: #fff;">
                    <i class="fa fa-camera"></i>
                    </v-btn>
                    <v-btn
                        elevation="2"
                        outlined
                        small
                        style="background-color: #fff;">
                        3D
                    </v-btn>
                    <v-btn
                        elevation="2"
                        outlined
                        small
                        style="background-color: #fff;">
                        2D
                    </v-btn>
                </div>
            </div>
        </aside>
    </div>
    <div v-else>
        <div class="fullbar__widget"
             :style="{'background-image':'url(https://nirvanaadikarya.id/wp-content/uploads/2020/06/Konsultan-Interior-Jakarta-Profesional-dan-Sangat-Berpengalaman.jpg)', 'background-size': 'cover', 'background-position': 'bottom'}">
            <v-btn
                v-model="fullSize"
                @click="toggleFullSize()"
                elevation="2"
                outlined
                small
                style="background-color: #fff;">
                <i class="fa fa-chevron-right"></i>
            </v-btn>
            <div style="margin-left: auto; padding-right: 20px;">
                <v-btn
                    elevation="2"
                    outlined
                    small
                    style="background-color: #fff;">
                    <i class="fa fa-camera"></i>
                </v-btn>
                <v-btn
                    elevation="2"
                    outlined
                    small
                    style="background-color: #fff;">
                    3D
                </v-btn>
                <v-btn
                    elevation="2"
                    outlined
                    small
                    style="background-color: #fff;">
                    2D
                </v-btn>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            fullSize: false,
            products: [1,2,3,4,5,6,7,8,9,10,11,12]
        }
    },
    methods: {
        toggleFullSize() {
            this.fullSize = !this.fullSize;
        }
    }
}
</script>

<style scoped>

</style>
