<template>
    <Header />
    <div class="gallery">
        <p class="title-indoor">INDOOR</p>
        <p class="des-indoor">Roller blinds - Vertical blinds - Roman blinds - Venetian blinds - Panel glide blinds - Curtains - Plantation Shutters</p>
        <div>
            <p class="roller-bind">ROLLER BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" style="margin-bottom: 20px;"> -->
                        <vue-picture-swipe :items="imageRollers" class="image-swipe"></vue-picture-swipe>
                    <!-- </MDBCol> -->
                <!-- </MDBRow> -->
            </div>
        </div>
        <div>
            <p class="roller-bind">VERTICAL BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageVerticals" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageVerticals" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">ROMAN BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageRomans" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageRomans" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">VENETIAN BLINDS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageVenetians" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageVenetians" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">CURTAINS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageCurtains" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageCurtains" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">PLANTATION SHUTTERS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imagePlantinos" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imagePlantinos" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <p class="title-indoor">OUTDOOR</p>
        <p class="des-indoor">Awnings - Zipscreen - Folding Arm Awnings</p>
        <div>
            <p class="roller-bind">AWNINGS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageAwnings" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageAwnings" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">ZIPSCREEN</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageZipSreens" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageZipSreens" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <div>
            <p class="roller-bind">FOLDING ARM AWNINGS</p>
            <div style="width: 100%; margin-top: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageFoldAwnings" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageFoldAwnings" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
        <p class="title-indoor">SECURITY</p>
        <p class="des-indoor">Roller Shutters - Security doors and Fly door - Security window (Security Grills) - Crimsafe - Fly screen/ Insect Screen</p>
        <div>
            <div style="width: 100%; margin-top: 20px; margin-bottom: 20px;">
                <!-- <MDBRow>
                    <MDBCol sm="6" md="3" lg="3" xl="3" v-for="(image, key) in imageSecuritys" :key="key" style="margin-bottom: 20px;">
                        <div class="col-example">
                            <div class="bg-image hover-zoom">
                                <img :src="image.src" class="image-gallery-roller img-fluid" />
                            </div>
                        </div>
                    </MDBCol>
                </MDBRow> -->
                <vue-picture-swipe :items="imageSecuritys" class="image-swipe"></vue-picture-swipe>
            </div>
        </div>
    </div>
    <Footer />
</template>
<script>
import Header from "@/views/Header.vue";
import Footer from "@/views/Footer.vue";
// import { MDBCol, MDBRow } from 'mdb-vue-ui-kit';
import VuePictureSwipe from 'vue-picture-swipe';
export default {
    name: "Home",
    components: { Header, Footer, VuePictureSwipe },
    data() {
        return {
            imageRollers: [
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Blockout-Roller-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/roller-blind-fancy-finish.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/roller-blind-fancy-finish.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Screen-Roller-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Screen-Roller-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageVerticals: [
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Vertical-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageRomans: [
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-3.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind-3.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Roman-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageVenetians: [
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Aluminium-Venetian-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Aluminium-Venetian-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Timber-Venetian-Blind.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Timber-Venetian-Blind.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageCurtains: [
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-3.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-3.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Curtain.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Sheer-Curtain.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Sheer-Curtain.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imagePlantinos: [
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-3.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter-3.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Plantation-Shutter.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageAwnings: [
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Crank-Straight-Drop-Awning.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Crank-Straight-Drop-Awning.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Fixed-Guide-Awning.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Fixed-Guide-Awning.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-1.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Wire-Guide-Awning-1.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageZipSreens: [
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Zipscreen.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageFoldAwnings: [
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Folding-Arm-Awning.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                }
            ],
            imageSecuritys: [
                {
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-2.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-2.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-3.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door-3.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
                { 
                    src: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door.jpg',
                    thumbnail: 'http://bwindowcovers.com.au/wp-content/uploads/2016/07/Security-Door.jpg',
                    w: 600,
                    h: 400,
                    alt: 'some numbers on a grey background'
                },
            ],
        };
    },
};
</script>

<style lang="scss">
    @media (min-width: 992px) {
        .image-swipe {
            img {
                width: 23%;
            }
        }
    }
    @media (max-width : 991px) {
        .image-swipe {
            img {
                width: 48%;
                margin-bottom: 10px;
            }
        }
    }
    
</style>
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