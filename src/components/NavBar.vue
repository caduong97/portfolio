<template>
    <div class="nav-container">

        <div class="name">
            <a class="" href="#">CA DUONG</a>
        </div>

        <div class="responsive-nav-button" v-on:click="openResponsiveNav"><i class="material-icons">menu</i></div>

        <div class="nav-items clearfix">
            <span v-on:click="scrollTo" class="underline"><b>Projects</b></span>
            <span v-on:click="scrollTo" class="underline"><b>Skill Set</b></span>
            <span v-on:click="scrollTo" class="underline"><b>Contact</b></span>
        </div>

        <div class="responsive-nav" v-bind:style="{display: displayResponsiveNav}">

            <div class="responsive-nav-button" v-on:click="closeResponsiveNav"><i class="material-icons">close</i></div>

            <div class="responsive-nav-items">
                <span v-on:click="scrollTo" class="underline" ><b>Projects</b></span><br/>
                <span v-on:click="scrollTo" class="underline"><b>Skill Set</b></span><br/>
                <span v-on:click="scrollTo" class="underline"><b>Contact</b></span><br/>
            </div>
        </div>

            
    </div>

    

</template>

<script>
    export default {
        name: "NavBar",

        data() {
            return {
                displayResponsiveNav: "none"
            }
        },

        methods: {
            scrollTo (event) {

                const targetName = event.target.innerText;
                console.log(event.target.innerText);

                const bodyRect = document.body.getBoundingClientRect();
                console.log(bodyRect);

                let toElement = null;

                
                switch (targetName) {
                    case "Projects":
                        toElement = document.getElementById("projects");
                        break;
                    case "Skill Set":
                        toElement = document.getElementById("skills");
                        break;
                    case "Contact":
                        toElement = document.getElementById("footer");
                        break;
                }
                // const element = document.getElementById('footer');

                const elemRect = toElement.getBoundingClientRect();
                console.log(elemRect);

                const offsetY = elemRect.top - bodyRect.top;
                console.log(offsetY);

                window.scrollTo({
                    top: offsetY,
                    left: 0,
                    behavior: 'smooth'
                });
            },

            openResponsiveNav() {
                this.displayResponsiveNav = "block";
            },

            closeResponsiveNav() {
                this.displayResponsiveNav = "none";
            }
        }

        
    }
</script>

<style lang="scss" scoped>

    .nav-container {
        width: 100%;
        height: 90px;
        z-index: 2;
        position: relative;

        .name {
            width: 150px;
            height: 100%;
            line-height: 80px;
            float: left;
            margin-left: 30px; 
        }

        .nav-items {
            float: right;
            height: 100%;
            width: 500px;
            line-height: 80px;
            padding-right: 30px; 
        }
    }

    .scrolling {
        background-color: rgba(29,29,37, 0.7);
    }

    .responsive-nav-button {
        color: #B0AFBD;
        float: right;
        height: 90px;
        margin-right: 30px;
        cursor: pointer;
        display: none;

        i {
            font-size: 3em;
            line-height: 80px;
        }

        &:hover {
            i {
                animation: flip-horizontal-bottom 0.7s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
            }
        }

    }

    .nav-items {
        color: #B0AFBD;
        display: inline;
        font-size: 1.3em;
        
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;

        cursor: pointer;
        
        & span {
            float: left;
            width: 500/3px;
            margin-left: 50px;
        }

    }

    .responsive-nav {
        color: #B0AFBD;
        width: 100vw;
        height: 90vh;
        background-color: #1D1D25;
        position: absolute;
        top: 0;
        left: 0;
        z-index: 4;
        animation: slide-right 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;

        // display: none;

        .responsive-nav-items {
            width: 300px;
            float: left;
            text-align: center;
            overflow: hidden;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            

            span {
                height: 200px;
                line-height: 80px;
                font-size: 1.5em;
            }
        }
    }

    .clearfix::after {
        content: "";
        clear: both;
        display: table;
    }

    .underline {
        transition: .5s;
        &:hover {
            color: white;
            border-bottom: 6px solid white;
            transition: ease .5s;
        }
    }

    @keyframes slide-right {
        0% {
            -webkit-transform: translateX(-200px);
                    transform: translateX(-200px);
        }
        100% {
            -webkit-transform: translateX(0px);
                    transform: translateX(0px);
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

    @media screen and (max-width: 700px) {
        .nav-items {
            display: none;
        }
        .responsive-nav-button {
            display: block;

            
        }


    }

    @media screen and (max-width: 500px) {
        .name {
            font-size: 0.8em;
        }
        .responsive-nav-button {
            margin-right: 20px;
            i {
                font-size: 2em;
            }

            &:active {

            }
        }
    }

    
    

</style>