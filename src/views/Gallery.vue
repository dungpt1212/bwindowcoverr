<template>
    <Header />
    <div class="gallery">
        <p class="title-indoor">INDOOR</p>
        <p class="des-indoor">Roller blinds - Vertical blinds - Roman blinds - Venetian blinds - Panel glide blinds - Curtains - Plantation Shutters</p>
        <div>
            <p class="roller-bind">ROLLER BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageRollers" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">VERTICAL BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageVerticals" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">ROMAN BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageRomans" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">VENETIAN BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageVenetians" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">CURTAINS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageCurtains" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">PLANTATION SHUTTERS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imagePlantinos" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <p class="title-indoor">OUTDOOR</p>
        <p class="des-indoor">Awnings - Zipscreen - Folding Arm Awnings</p>
        <div>
            <p class="roller-bind">AWNINGS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageAwnings" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">ZIPSCREEN</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageZipSreens" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <div>
            <p class="roller-bind">FOLDING ARM AWNINGS</p>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageFoldAwnings" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
        <p class="title-indoor">SECURITY</p>
        <p class="des-indoor">Roller Shutters - Security doors and Fly door - Security window (Security Grills) - Crimsafe - Fly screen/ Insect Screen</p>
        <div>
            <div style="width: 100%; margin-top: 20px;">
                <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageSecuritys" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.url" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow>
            </div>
        </div>
    </div>
    <Footer />
</template>
<script>
import Header from "@/views/Header.vue";
import Footer from "@/views/Footer.vue";
import { MDBCol, MDBRow } from 'mdb-vue-ui-kit';
export default {
    name: "Home",
    components: { Header, Footer, MDBCol, MDBRow },
    data() {
        return {
            imageRollers: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/roller-blind-fancy-finish.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Screen-Roller-Blind.jpg' }
            ],
            imageVerticals: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind.jpg' }
            ],
            imageRomans: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-3.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind.jpg' }
            ],
            imageVenetians: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Aluminium-Venetian-Blind.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Timber-Venetian-Blind.jpg' }
            ],
            imageCurtains: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-3.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Sheer-Curtain.jpg' }
            ],
            imagePlantinos: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-3.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter.jpg' }
            ],
            imageAwnings: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Crank-Straight-Drop-Awning.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Fixed-Guide-Awning.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-1.jpg' }
            ],
            imageZipSreens: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen.jpg' }
            ],
            imageFoldAwnings: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning.jpg' }
            ],
            imageSecuritys: [
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-2.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-3.jpg' },
                { url: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door.jpg' },
            ],
        };
    },
};
</script>

<style lang="scss" scoped>
    .row {
        --mdb-gutter-x: 0;
    }
    .gallery {
        padding-top: 160px;
        text-align: center;
        .title-indoor {
            font-size: 36px;
            font-weight: 200;
            color: #1d1d1d
        }
        .des-indoor {
            color: #999999;
            font-size: 16px;
        }
        .roller-bind {
            color: #d80808;
            font-size: 22px;
            width: 100%;
            font-weight: 200;
        }
        .image-gallery-roller {
            cursor: pointer;
            width: 100%;
        }
        .col-example {
            padding: 0 10px;
        }
    }
</style>