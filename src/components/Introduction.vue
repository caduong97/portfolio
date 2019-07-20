<template>
    <div class="opening">
        <div class="introduction">
            <h3><b>Hello, I am Ca Duong </b></h3>
            <p></p>
            <p>I am a <span>&nbsp;junior Frond-end Developer&nbsp;</span> who is currently located in Finland. <br/>
                I have just finished my third year as a Business Information Technology student at Lahti University of Applied Sciences. 
                I am particularly interested in <span>&nbsp;Javascript&nbsp;</span>, both Vanilla JS and libraries such as React.js, JQuery, Vue.js, etc. 
                I have also had experience with back-end coding in PHP and Node.js as well as databases including MySQL and MongoDB</p>
            <button class="button" @click='onClick'><span><b>Let's talk</b></span></button>
        </div>

        

        <ul>
            <li><a href="https://github.com/caduong97" target="_blank"><i class="fab fa-github"></i></a></li>
            <li><a href="https://www.linkedin.com/in/ca-duong-901710143/" target="_blank"><i class="fab fa-linkedin"></i></a></li>
            <li><a href="https://drive.google.com/file/d/1HIJsbWsb3rNGnknyBx0MZ_osRetd9gKS/view?usp=sharing" target="_blank"><i class="far fa-sticky-note"></i></a></li>
        </ul>
        
        <div v-on:click="scrollTo" class="scroll-down"><i class="fas fa-sort-down"></i></div>
    </div>

</template>

<script> 
    export default {
        name: "Introduction",
        props: {
            onClick: Function
        },
        data () {
            return {
                isScrolling: true
            }    
        },
        methods: {
            scrollTo () {
                window.scrollTo({
                    top: 950,
                    left: 0,
                    behavior: 'smooth'
                });
            }
        }
        // ,
        // created () {
        //     window.addEventListener('scroll', this.handleScroll);
        // },
        // destroyed () {
        //     window.removeEventListener('scroll', this.handleScroll);
        // }

    }
</script>

<style lang="scss" scoped>
    .opening {
        background-color: #1D1D25;
        position: relative;
        
        top: -90px;
        left: 0;
        margin-bottom: -90px;
        width: 100%;
        height: 100vh;
        
        

    }

    .introduction {
        width: 900px;
        color: #B0AFBD;

        position: absolute;
        top: 50%;
        transform: translateY(-50%);

        margin-left: 300px;
        line-height: 2.5em;
        animation: show-up 1.5s;
        
        
        & p {
            font-size: 1.3em;
        }

        & span {
            color: white;
        }


    }

    ul {
        color: #B0AFBD;
        
        z-index: 2;
        
        list-style-type: none;
        margin: 0;
        padding: 0;
        // padding-right: 20px;
        
        position: absolute;
        // position: fixed;
        top: 50%;
        right: 0;
        transform: translateY(-50%);

        cursor: pointer;

        li {
            font-size: 2.5em;
            padding-right: 20px;
            padding-left: 20px;
            margin-top: 3px;
            

            a {
                color: #B0AFBD;
                transition: .3s ;
                &:hover {
                    color: white;
                    transition: .3s ;
                }
            }
            

        }

    }


    button {
        width: 150px;
    }

    .scroll-down {
        color: #B0AFBD;
        font-size: 4em;
        width: 100%;
        position: absolute;
        text-align: center;
        bottom: 0;

        transition: .3s ;
        &:hover {
            color: white;
            transition: .3s ;
        }
        
    }

    

    @keyframes show-up {
        0% {
            opacity: 0.3;
        }
        100% {
            opacity: 1;
        }
    }


    @media screen and (max-width: 1400px) {
        .introduction {
            margin-left: 200px;
        }
    }

    @media screen and (max-width: 1300px) {
        .introduction {
            margin-left: 100px;
        }
    }

    @media screen and (max-width: 1200px) {
        .introduction {
            margin-left: 80px;

        }
    }

    @media screen and (max-width: 1100px) {
        .introduction {
            width: 800px;

            h3 {
                font-size: 1.3em;
            }

            p {
                font-size: 1.1em;
            }
        }
    }

    @media screen and (max-width: 1000px) {
        .introduction {
            width: 700px;
        }
    }

    @media screen and (max-width: 900px) {
        // .opening {
            .introduction {
                width: 600px;
            }

            .scroll-down {
                font-size: 3em;
                
            }
        // }
    }

    

    @media screen and (max-width: 800px) {
        .introduction {
            width: 500px;

            h3 {
                font-size: 1.2em;
            }

            p {
                font-size: 1em;
            }

        }
        a {
            font-size: 1em;
        }
            
        
    }

    @media screen and (max-width: 600px) {
        .opening {
            height: 95vh;
        }

        .introduction {
            margin-left: 50px;
            width: 400px;

            

        }
        a {
            font-size: 1em;
        }
    }

    @media screen and (max-width: 500px) {

        .introduction {
            margin-left: 30px;
            width: 70vw;
            line-height: 1.7em;

            h3 {
                font-size: 1em;
            }

            p {
                font-size: 0.8em;
            }
        }

        .scroll-down {
                font-size: 2.5em;
                
        }

    }



</style>