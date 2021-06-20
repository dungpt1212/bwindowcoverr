<template>
    <Header />
    <div class="gallery">
        <p class="title-indoor">INDOOR</p>
        <p class="des-indoor">Roller blinds - Vertical blinds - Roman blinds - Venetian blinds - Panel glide blinds - Curtains - Plantation Shutters</p>
        <p class="roller-bind">ROLLER BLINDS</p>
        <MDBRow>
            <MDBCol sm="" md="4" v-for="(image, key) in imageRollers" :key="key">
                <div>
                    <img :src="image.url" />
                </div>
            </MDBCol>
        </MDBRow>
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
            ]
        };
    },
};
</script>

<style lang="scss" scoped>
    .gallery {
        height: 100vh;
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
    }
</style>