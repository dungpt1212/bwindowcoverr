<template>
    <Header />
    <div class="contact-background">
        <p>Reach Us At</p>
    </div>
    <div style="width: 80%; margin: 0px auto;" class="contact-page">
        <MDBRow class="mt-5 mb-5">
            <MDBCol>
                <h5 style="font-weight:100">We love to listen and we are eagerly waiting to talk to you regarding your project. Post any queries you have and we will get back to you as soon as possible.</h5>
            </MDBCol>
        </MDBRow>
        <MDBRow>
            <MDBCol sm="12" md="12" lg="4" xl="4" @mouseover="showContent(1)" @mouseleave="hideContent(1)" style="padding-left: 0px;">
                <a href="#">
                    <div class="animate-icon-module">
                        <i class="fas fa-map-marker-alt icon icon1"></i>
                        <p class="font-100 content content1">
                            1/52 Smith Road,Springvale,Vic 3171Weekdays<br>
                            9am – 4pm Weekends by appointment
                        </p>
                    </div>
                </a>
            </MDBCol>
             <MDBCol sm="12" md="12" lg="4" xl="4" @mouseover="showContent(2)" @mouseleave="hideContent(2)" style="padding-left: 0px;">
                <a href="#">
                    <div class="animate-icon-module">
                        <i class="fas fa-envelope icon icon2"></i>
                        <p class="font-100 content content2">
                            bwindowcovers@gmail.com
                        </p>
                    </div>
                </a>
            </MDBCol>
             <MDBCol sm="12" md="12" lg="4" xl="4" @mouseover="showContent(3)" @mouseleave="hideContent(3)" style="padding-left: 0px;">
                <a href="#">
                    <div class="animate-icon-module">
                        <i class="fas fa-phone-alt icon icon3"></i>
                        <p class="font-100 content content3">
                            (03) 8502 7472
                        </p>
                    </div>
                </a>
            </MDBCol>
        </MDBRow>
         <MDBRow class="mt-5 mb-5">
            <MDBCol sm="12" md="12" lg="6" xl="6">
                <h6 class="text-start font-150">POST YOUR QUERY</h6>
                <MDBRow tag="form" class="g-3 needs-validation" novalidate @submit.prevent="checkForm">
                    <MDBInput label="Name" size="lg" invalidFeedback="Please provide Name." required />
                    <MDBInput label="Email" class="mt-4" size="lg" invalidFeedback="Please provide Email." required />
                    <MDBInput label="Subject" class="mt-4" size="lg" invalidFeedback="Please provide Subject." required />
                    <MDBTextarea label="Message" rows="4" class="mt-4 mb-5" invalidFeedback="Please provide Message." required />
                    <div style="text-align: left; margin-bottom: 20px;">
                        <MDBBtn color="dark" class="mt-4" size="lg" type="submit">SUBMIT</MDBBtn>
                    </div>
                </MDBRow>
            </MDBCol>
            <MDBCol sm="12" md="12" lg="6" xl="6">
                <h6 class="text-start font-100 mb-5">OUR OFFICE</h6>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d953718.7081295741!2d105.09215784260898!3d20.974041527113535!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3135008e13800a29%3A0x2987e416210b90d!2zSMOgIE7hu5lpLCBWaeG7h3QgTmFt!5e0!3m2!1svi!2s!4v1624300856938!5m2!1svi!2s" height="450" style="border:0; width: 100%;" allowfullscreen="" loading="lazy"></iframe>
            </MDBCol>
        </MDBRow>
    </div>
    <Footer />
</template>
<script>
import Header from "@/views/Header.vue";
import Footer from "@/views/Footer.vue";
import { MDBCol, MDBRow, MDBInput, MDBTextarea, MDBBtn } from 'mdb-vue-ui-kit';
import $ from 'jquery';

export default {
    name: "Indoor",
    components: { Header, Footer, MDBCol, MDBRow, MDBInput, MDBTextarea, MDBBtn },
    data() {
        return {
            
        };
    },
    setup() {
        const checkForm = e => {
            e.target.classList.add("was-validated");
        };
        return {
            checkForm
        };
    },
    methods: {
        showContent (index) {
            $('.animate-icon-module .icon.icon' + index).removeClass('show');
            $('.animate-icon-module .icon.icon' + index).addClass('hide');
            $('.animate-icon-module .content.content' + index).removeClass('hide');
            $('.animate-icon-module .content.content' + index).addClass('show');
        },
        hideContent (index) {
            $('.animate-icon-module .icon.icon' + index).removeClass('hide');
            $('.animate-icon-module .icon.icon' + index).addClass('show');
            $('.animate-icon-module .content.content' + index).removeClass('show');
            $('.animate-icon-module .content.content' + index).addClass('hide');
        }
    }
};
</script>
<style lang="scss">
    .form-outline {
        margin-bottom: 15px;
    }
    .invalid-feedback {
        margin-top: 8px;
    }
</style>
<style lang="scss" scoped>
    .contact-background {
        background: url(http://bwindowcovers.com.au/wp-content/uploads/2014/11/bg1.jpg) center center no-repeat scroll;
        height: 500px;
        opacity: 1;
        padding: 0px;
        position: relative;
        p {
            position: absolute;
            top: 40%;
            right: 37%;
            color: #ffffff;
            font-size: 50px;
            font-weight: 100;
            font-size: 70px;
        }
    }
    .contact-page {
        .animate-icon-module {
            background: #f2f4f8;
            margin-bottom: 20px;
            height: 200px;
            position: relative;
            overflow: hidden;
            .icon {
                position: absolute;
                top: 75px;
                color: #d80808;
                font-size: 50px;
                left: 45%;
                transition: 0.5s;
            }
            .content {
                color: #d80808;
                position: absolute;
                width: 100%;
                bottom: -150px;
                left: 0px;
                transition: 0.5s;
            }
            .icon.hide {
                top: -100px;
            }
            .icon.show {
                top: 75px;
            }
            .content.show {
                bottom: 30%;
            }
            .content.hide {
                bottom: -200px;
            }
        }
        .font-100 {
            font-weight: 100;
        }
    }
</style>