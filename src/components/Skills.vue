<template>
    <div>
        <img src="@/assets/images/code-coder-coding-270348.jpg" alt="tech" />

        
        <h1 id="skills">Skill set</h1>
        
        <div class="skills">

            <div class="skill clearfix">
                <div class="skill-title">
                    <h4><i class="far fa-file-code"></i>&nbsp;&nbsp;Programming</h4>
                </div>

                <div class="skill-list-1">
                    <span class="underline">HTML</span><br/>
                    <span class="underline">CSS</span><br/>
                    <span class="underline">SCSS</span><br/>
                    <span class="underline">Vanilla JS</span><br/>
                    <span class="underline">React.js</span><br/>
                </div>

                <div class="skill-list-2">
                    <span class="underline">Redux</span><br/>
                    <span class="underline">jQuery</span><br/>
                    <span class="underline">Vue.js</span><br/>
                    <span class="underline">Bootstrap</span><br/>
                    <span class="underline">PHP</span><br/>                    
                </div>

            </div>

            <div class="skill clearfix">
                <div class="skill-title">
                    <h4><i class="fas fa-database"></i>&nbsp;&nbsp;Databases</h4>
                </div>

                <div class="skill-list-1">
                    <span class="underline">MySQL</span><br/>
                </div>
                <div class="skill-list-2">
                    <span class="underline">MongoDB</span><br/>
                </div>
            </div>

            <div class="skill clearfix">
                <div class="skill-title">
                    <h4><i class="fas fa-crop"></i>&nbsp;&nbsp;Visual</h4>
                </div>

                <div class="skill-list-1">
                    <span class="underline">Procreate</span>  
                    <br/>
                    <span class="underline">Adobe Premiere Pro</span>  
                    <br/>
                    <span class="underline">Adobe Lightroom</span>
                </div>
                <div class="skill-list-2">
                    <span class="underline">Prototype tools</span>  
                    <br/>
                        <span class="underline">Framer</span>  
                        <br/>
                        <span class="underline">Figma</span>  
                        <br/>
                </div>
            </div>
            <div class="skill clearfix">
                <div class="skill-title">
                    <h4><i class="fas fa-desktop"></i>&nbsp;&nbsp;Digital </h4>
                </div>

                <div class="skill-list-1">
                    <span class="underline">Google Drive</span> 
                    <br/>
                    <span class="underline">Microsoft Office</span>
                </div>
                <div class="skill-list-2">
                    <span class="underline">One Drive</span>  
                    <br/>
                    <span class="underline">Dropbox</span>  
                </div>
            </div>

        </div>

    </div>
    
</template>

<script>
    export default {
        name: "Skills"
    }
</script>

<style lang="scss" scoped>
    img {
        width: 100%;
        height: 700px;
        object-fit: cover;
        // margin-bottom: 100px;
        
    }

    h1 {
        padding-top: 100px;
        text-align: center;
        padding-bottom: 50px;
    }

    h4 {
        font-weight: 600;
        letter-spacing: 0.1em;
        color:#1D1D25;
        opacity: 0.8;
    }

    .skills {
        width: 900px;
        margin: 0 auto;
        padding-bottom: 100px;
        

        .skill {
            width: 100%;
            padding-bottom: 30px;

            .skill-title {
                width: 300px;
                float: left;
                
            }

            .skill-list-1 {
                width: 300px;
                float: left;
                line-height: 2.5em;
                text-align: center;
            }

            .skill-list-2 {
                width: 300px;
                float: left;
                line-height: 2.5em;
                text-align: center;
            }

        }


    }

    

    .underline {
        cursor: pointer;
        padding-bottom: 3px;
        text-align: center;
        &:hover {
            border-bottom: 6px solid #1D1D25;
            transition: ease .1s;
            
        }
    }

    

    .clearfix::after {
        content: "";
        clear: both;
        display: table;
    }

    @media screen and (max-width: 1000px) {
        img {
            width: 100%;
            height: 500px;
            object-fit: cover;
        }

        .skills {
            width: 800px;

            .skill {
                .skill-title {
                    width: 33.4%;
                }

                .skill-list-1 {
                    width: 33.3%;
                }

                .skill-list-2 {
                    width: 33.3%;
                }
            }
        }


    }

    @media screen and (max-width: 900px) {
        .skills {
            width: 700px;

            .skill {
                .skill-title {
                    width: 33.4%;

                    h4 {
                        font-size: 1.2em;
                    }
                }

                .skill-list-1 {
                    width: 33.3%;

                    span {
                        font-size: 0.9em;
                    }
                }

                .skill-list-2 {
                    width: 33.3%;

                    span {
                        font-size: 0.9em;
                    }
                }
            }
        }
    }



    @media screen and (max-width: 800px) {
        img {
            width: 100%;
            height: 300px;
        }

        .skills {
            width: 600px;

            .skill {
                .skill-title {
                    width: 33.4%;

                    h4 {
                        font-size: 1.1em;
                    }
                }

                .skill-list-1 {
                    width: 33.3%;

                    span {
                        font-size: 0.8em;
                    }
                }

                .skill-list-2 {
                    width: 33.3%;

                    span {
                        font-size: 0.8em;
                    }
                }
            }
        }
    }



    @media screen and (max-width: 500px) {
        img {
            width: 100vw;
            height: 250px;
            margin-top: -60px;
        }

        .skills {
            width: 80%;

            .skill {
                .skill-title {
                    width: 100%;

                    h4 {
                        font-size: 1.1em;
                    }
                }

                .skill-list-1 {
                    width: 50%;
                    line-height: 2em;

                    span {
                        font-size: 0.8em;
                    }
                }

                .skill-list-2 {
                    width: 50%;
                    line-height: 2em;

                    span {
                        font-size: 0.8em;
                    }
                }
            }
        }

        
    }

    
</style>