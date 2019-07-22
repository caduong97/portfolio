

<template >
    <div v-if="showContactForm" class="contact">
        <div class="contact-container">
            <div class="about-me">
                <img src="@/assets/images/IMG_0995.jpg" alt="my-portrait" >

                <div>
                    <p>I am a 22-year-old Vietnamese, now studying in Finland. I love everything about art: I draw, paint, and do digital art. I also love music and play a bit of guitar and piano. 
                        I am seeking for a frond-end developing internship in Finland, starting as soon as possible.</p>

                    <p class="write-mes">Scroll down to write a message to me&nbsp;&nbsp;<i class="fas fa-sort-down"></i></p>
                </div>
            </div>

            <div class="contact-form">
                <!-- gg icons -->

                <i @click="onClick" class="material-icons">close</i>

                <!-- <p>Write to me, an offer, a suggestion, or even a constructive advice is still very welcomed ! </p> -->
                

                <form :class="{ formSubmitted: formSubmitted }" id="contact-form" v-if="!isLoading">

                    <div v-if="formInvalid" class="invalid-notice"><b>*&nbsp;&nbsp;Please fill in all required fields</b></div>

                    <input type="hidden" v-model="contact_number" v-if="!formSubmitted">

                    <label for="name"><b>Your name&nbsp;&nbsp;*</b></label><br/>
                    <input type="text" v-model="name"><br/>
                    <label for="email"><b>Your email&nbsp;&nbsp;*</b></label><br/>
                    <input type="text" v-model="email"><br/>
                    <!-- <label>to_name</label> -->
                    <!-- <input type="hidden" name="to_name" /> -->
                    <label for="message" ><b>Message&nbsp;&nbsp;*</b></label><br/>
                    <textarea v-model="message"></textarea>
                    
                    <button v-if="!isLoading" type="submit" class="button" v-on:click="submit"><span><b>Send</b></span></button>
                    <!-- <button v-else type="submit" class="button"><b>Sending...</b></button> -->
                </form>

                <div v-if="formSubmitted" class="response">Thank you! Your message has been sent.</div>
            </div>
        </div>
    </div>
</template>



<script>
    export default {
        name: "ContactForm",
        props: {
            showContactForm: Boolean,
            
            onClick: Function
        
        },

        data() {
            return {
                show: false,

                //datas below regarding the contact form 
                contact_number: null,
                name: '',
                email: '',
                message: '',
                formSubmitted: false,
                isLoading: false,
                formInvalid: false
            }
        },
        mounted () {
            this.$nextTick(function () {
            let emailJSscript = document.createElement('script')
            emailJSscript.setAttribute('src', 'https://cdn.emailjs.com/sdk/2.3.2/email.min.js')
            document.head.appendChild(emailJSscript)
            })

            
        },

        methods: {
            submit () {
                event.preventDefault()
                if (this.email !== '' && this.name !== '' && this.message !== '' ) {
                    this.formInvalid = false
                    this.isLoading = true
                    this.formSubmitted = false
                    emailjs.init('user_7pcfIpeHVeMSLH6OpFate')
                    this.contact_number = Math.random() * 100000 | 0

                    emailjs.send(
                    'contact_service',
                    'template_F67PEpUV',
                    {from_email: this.email, from_name: this.name, message_html: this.message}
                    ).then((response) => {
                    this.formSubmitted = true
                    this.isLoading = false
                    
                    console.log('SUCCESS You just sent an email...', response)
                    console.log(this.name + ", " + this.email + ', ' + this.message)
                    this.name = ''
                    this.email = ''
                    this.message = ''
                    }, (error) => {
                    console.log('FAILED Throw an error to user...', error)
                    this.isLoading = false
                    })
                } else {
                    this.formInvalid = true
                }
            }
        }
    }

</script>

<style lang="scss" scoped>
    .contact {
        width: 100%;
        height: 100vh;
        background-color:  rgba(51, 51, 61, 0.8);
        z-index: 3;
        position: relative;
        position: fixed;
        top: 0;

            .contact-container {
                width: 1000px;
                height: 750px;
                margin: 0 auto;
                // z-index: 3;

                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                // transition: ease 2s;
                
                .about-me {
                    width: 50%;
                    height: 100%;
                    float: left;
                    background-color: #B0AFBD;
                    animation: slide-from-top 0.9s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
                    padding: 30px;
                    line-height: 1.8em;
                    img{
                        width: 100%;
                        height: auto;
                        border-radius: 8px;
                        margin-bottom: 20px;
                    }

                    .write-mes {
                        display: none;
                    }


                    
                }

                .contact-form {
                    width: 50%;
                    height: 100%;
                    float: left;
                    background-color: #1D1D25;
                    animation: slide-from-bottom 0.9s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
                    padding: 30px;

                    
                    i {
                        color: white;
                        font-size: 2.5em;
                        position: absolute;
                        top: 30px;
                        right: 30px;
                        cursor: pointer;

                        &:hover {
                            animation: flip-horizontal-bottom 0.7s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
                            // opacity: 0.5;
                        }
                    }

                    

                    form {

                        color: white;
                        position: relative;
                        top: 50px;
                        
                        .invalid-notice {
                            font-size: 0.8em;
                            margin-top: 20px;
                            color: white;
                            margin-bottom: 20px;
                        }


                        label {
                            line-height: 2em;
                        }

                        input {
                            width: 100%;
                            border: none;
                            border-bottom: 3px solid white;
                            background-color: #1D1D25;
                            outline: none;
                            margin-bottom: 30px;

                            
                        }

                        textarea {
                            width: 100%;
                            height: 150px;
                            border: none;
                            border-bottom: 3px solid white;
                            background-color: #1D1D25;
                            color: white;
                            outline: none;
                            margin-bottom: 30px;
                        }

                        input[type=text] {
                            color: white;
                            
                        }

                        button {
                            margin-top: 20px;
                            width: 120px;
                            line-height: 50px;

                            i {
                                font-size: 2em;
                                height: 50px;
                                line-height: 50px;
                            }
                            
                        }

                    }

                    .response {
                        margin-top: 80px;
                        color: white;
                    }

                }
            }
    }

    @keyframes slide-from-top {
        0% {
            -webkit-transform: translateY(-400px);
                    transform: translateY(-400px);
        }
        100% {
            -webkit-transform: translateY(0);
                    transform: translateY(0);
        }
    }

    @keyframes slide-from-bottom {
        0% {
            -webkit-transform: translateY(400px);
                    transform: translateY(400px);
        }
        100% {
            -webkit-transform: translateY(0);
                    transform: translateY(0);
        }
    }

    @keyframes flip-horizontal-bottom {
        0% {
            -webkit-transform: rotateX(0);
                    transform: rotateX(0);
        }
        100% {
            -webkit-transform: rotateX(-180deg);
                    transform: rotateX(-180deg);
        }
    }

    @keyframes shadow-drop-center {
        0% {
            box-shadow: 0 0 0 0 rgba(0, 0, 0, 0);
        }
        100% {
            box-shadow: 0 0 20px 0px rgba(0, 0, 0, 0.35);
        }
    }

    @media screen and (max-width: 1000px) {
        .contact {
            .contact-container {
                width: 800px;
            }
        }
        
    }

    @media screen and (max-width: 800px) {
        .contact {
            .contact-container {
                width: 500px;
                overflow: scroll;
                

                .about-me {
                    width: 100%;
                        
                    div {
                        font-size: 0.9em;
                    }
                    
                    


                    .write-mes {
                        text-align: center;
                        font-weight: 600;
                        font-size: 1em;
                        display: block;

                    }
                }

                .contact-form {
                    width: 100%;

                    form {

                        input[type=text] {
                            font-size: 0.9em;
                        }

                        button {
                            line-height: 40px;
                        }
                    }

                }
            }
        }
        
    }

    @media screen and (max-width: 600px) {
        .contact {
            .contact-container {
                width: 100vw;
                // font-size: 0.8em;

                .about-me {
                    display: none;
                }

                .contact-form {

                    form {
                        label {
                            font-size: 0.8em;
                        }
                    }
                    
                }
            }
        }
    }


</style>

