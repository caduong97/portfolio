<template>
    <div class="footer-container" id="footer">
        <div class="footer">
            <table class="contact-info">
                <tr>
                    <td>
                        <p><b>Please contact me via: </b>
                        <br/>
                        <i class="far fa-envelope"></i>&nbsp;&nbsp;Email: <a class="email" href="mailto:duonghotinhca.97@gmail.com">duonghotinhca.97@gmail.com</a>
                        <br/>
                        <i class="fas fa-mobile-alt"></i>&nbsp;&nbsp;Phone:  <a class="phoneNum" href="#">+358 457 875 7880</a>
                        <br/>
                        <i class="fab fa-linkedin"></i>&nbsp;&nbsp;LinkedIn: <a class="linkedin" href="https://www.linkedin.com/in/ca-duong-901710143/" target="_blank">Ca Duong</a></p>
                        
                    </td>
                </tr>
            </table>


            <table class="contact-form">
                <tr>
                    <td>
                        <span><b>Or write something to me</b> &nbsp;&nbsp;
                            <button class="button" @click='onClick'><span><b>here</b></span></button>
                        </span>
                        <br/>
                        &nbsp;
                        <br/>
                        &nbsp;
                        <br/>
                        <span>&copy; 2019 Ca Duong </span>
                    </td>
                </tr>
            </table>

        </div>
    </div>
</template>

<script>
    export default {
        name: "Footer",
        props: {
            onClick: Function
        }
    }
</script>

<style lang="scss" scoped>
    .footer-container {
        width: 100%;
        height: 300px;
        background-color: #1D1D25;
        color: #B0AFBD;
        font-size: 1.1em;

        .footer {
            width: 900px;
            margin: 0 auto;
            

            .contact-info {
                width: 50%;
                height: 300px;
                float: left;
                padding-left: 100px;
                line-height: 2.5em;
            }

            .contact-form {
                width: 50%;
                float: left;
                height: 300px;
                line-height: 2.5em;
                text-align: right;
                border-left: 0.1px solid #B0AFBD;
            }
        }

        
    }

    button {
        // background-image: linear-gradient(to right, #3084c5, #4796c9, #62a7cc, #80b7cf, #9ec6d3);
        // color: white;
        // border-radius: 4px;
        width: 120px;
        // height: 50px;
        
        // span {
        //     cursor: pointer;
        //     display: inline-block;
        //     position: relative;
        //     transition: 0.5s;

        //     &:after {
        //         content: '\00bb';
        //         font-weight: 700;
        //         font-size: 1.5em;
        //         position: absolute;
        //         opacity: 0;
        //         top: -1px;
        //         right: -20px;
        //         transition: 0.5s;
        //     }
        // }

        // &:hover {
        //     span {
        //         padding-right: 25px;

        //         &:after {
        //             opacity: 1;
        //             right: 0;
        //         }
        //     }

            
        // }
    }


    a {
        font-size: 1em;
        &:hover {
            color: white;
            font-weight: 700;
            text-decoration: none;
        }
    }

    .email {
        text-decoration: underline;

        &:hover {
            text-decoration: underline;
        }     
    }

    @media screen and (max-width: 1000px) {
        .footer-container {
            width: 100%;
            height: 500px;
            font-size: 1em;

            .footer {
                width: 600px;

                .contact-info {
                    width: 100%;
                    height: 250px;
                }

                .contact-form {
                    width: 100%;
                    height: 250px;
                    border:none;
                    
                }

            }
        }
        
    }

    @media screen and (max-width: 800px) {
        .footer-container {
            
            height: 400px;
            font-size: 0.9em;

            .footer {
                width: 400px;

                .contact-info {
                    width: 100%;
                    height: 230px;
                }

                .contact-form {
                    width: 100%;
                    height: 170px;
                    
                }

            }
        }
    }

    @media screen and (max-width: 500px) {
        .footer-container {
            
            height: 400px;
            font-size: 0.8em;

            .footer {
                width: 90%;

                .contact-info {
                    width: 100%;
                    height: 230px;
                }

                .contact-form {
                    width: 100%;
                    height: 170px;
                }

            }
        }
    }



</style>

