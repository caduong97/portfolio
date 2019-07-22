<template>
    <div class="projects" id="projects">

        
        <h1>Latest projects</h1>
        


        <div class="project-1">
            <div class="img-container">
                <img src="@/assets/images/SELLGAMES_logo.png" alt="sellgames2020" />
                <img class="overlay" src="@/assets/images/sellgames-cap.png" alt="sellgames2020" />
            </div>

            <div class="clearfix">
                <div class="project-title">
                    <h3>Real-life IT Project</h3>
                    <h5><em>SELL GAMES 2020 Website</em></h5>
                    <p><small>(Unfortunately, the project's repository has to be kept private until the event will happen next year)</small></p>
                </div>

                <div class="project-description">
                    <p>I took a course named Real-life IT Project and Practices in which we designed and coded for SELLGAMES 2020 - a real student sport competition.<br/>
                        The project aimed for a user-friendly, cooperative, not just informative but also dynamic website to present information and news about the SELL GAMES 2020 event. <br/>
                        Tech stack: React.js, CSS, SCSS, Express, Node.js, NPM, MongoDB, Mongoose <br/>
                        My role: a designer and a front-end developer <br/>
                    </p>
                </div>
            </div>

        </div>

        <div class="project-1">
            <div class="img-container">
                <img src="@/assets/images/HACMA-main-page.png" alt="hacma" />
                <!-- <div class="overlay"> -->
                    <!-- <div class="text">Click to see more about the project</div> -->
                    <img class="overlay" src="@/assets/images/hacma-login.jpg" alt="hacma" />
                <!-- </div> -->
            </div>

            <div class="clearfix">
                <div class="project-title">
                    <h3>Agile WebApp Development Project</h3>
                    <h5><em>HACMA Mobile Carrier WebApp</em></h5>
                    <a href="https://github.com/anlissy/HACMA" target="_blank">
                        <button class="button">
                        
                            <span><b>project repository</b></span>
                        
                        </button>
                    </a>
                </div>

                <div class="project-description">
                    <p>Agile Web Application Development Project is a project course where we applied the theory of agile software development methods to a group work project, aiming to develop an application of our preference. <br/>
                        Our group created a mobile carrier application, which allow users to check up on their current prepaid package and top up or buy another packages as they wish. <br/>
                        Tech stack: HTML, CSS, PHP, MySQL <br/>
                        My role: a designer and a front-end + back-end developer <br/>
                    </p>
                    <br/>
                </div>
            </div>


        </div>


        <div class="project-1">
            <div class="img-container">
                <img src="@/assets/images/blog-cap.jpg" alt="personal-site-project" />
                <img class="overlay" src="@/assets/images/blog-photos-cap.png" alt="personal-site-project"/>
                    
                
            </div>

            <div class="clearfix">
                <div class="project-title">
                    <h3>Personal Project</h3>
                    <h5><em>A blog site</em></h5>
                    <a href="https://github.com/caduong97/personal-blog" target="_blank">
                        <button class="button">
                        
                            <span><b>project repository</b></span>
                        
                        </button>
                    </a>
                    <!-- <a href="https://github.com/caduong97/personal-blog" target="_blank">
                        <button class="button">
                        
                            <span><b>project view</b></span>
                        
                        </button>
                    </a> -->
                </div>

                <div class="project-description">
                    <p>This is a personal project I did on my own for studying purpose.<br/>
                        The website was build using mostly React.js. This project is an ongoing project and currently it is merely about the interface. 
                        I plan to expand it more by adding admin functions so as it works like a real blog. 
                        <br/>
                        <br/>
                    </p>
                </div>
            </div>

        </div>

        <div class="project-1">
            <div class="img-container">
                <img src="@/assets/images/drum-machine.png" alt="drum-machine" />
                <!-- <div class="overlay">
                    <div class="text">Click to see more about the project</div>
                </div> -->
            </div>

            <div class="clearfix">
                <div class="project-title">
                    <h3>Personal Project</h3>
                    <h5><em>A drum machine</em></h5>
                    <a href="https://github.com/caduong97/drum-machine" target="_blank">
                        <button class="button">
                        
                            <span><b>project repository</b></span>
                        
                        </button>
                    </a>
                    <a href="https://caduong97.github.io/drum-machine/" target="_blank">
                        <button class="button">
                        
                            <span><b>project view</b></span>
                        
                        </button>
                    </a>
                </div>

                <div class="project-description">
                    <p>This is also a personal project I did on my own for studying purpose.<br/>
                        The project was done with vanilla JavaScript. The drum pad can be triggered by clicking the corresponding key pad.
                        <br/>
                        <br/>
                        <br/>
                        <br/>
                    </p>
                </div>
            </div>

        </div>

    </div>
    

</template>

<script>


    export default {
        name: 'Projects'
    }
</script>

<style lang="scss">
    .projects {
        padding-top: 100px;

        h1 {
            text-align: center;
            padding-bottom: 100px;
        }

        .project-title {
            width: 400px;
            float: left;
            padding-right: 30px;

            h3 {
                font-weight: 600;
                letter-spacing: 0.1em;
                line-height: 2em;
                color:#1D1D25;
                opacity: 0.8;
            }


            a {
                font-size: 1em;
                color: white;

                button {
                    margin-top: 20px;
                    width: 250px;
                    line-height: 50px;

                    i {
                        font-size: 2em;
                        height: 50px;
                        line-height: 50px;
                    }
                    
                }
            }
            
            
        }

        .project-description {
            width: 500px;
            float: left;
            line-height: 2em;
            padding-bottom: 70px;
        }

        .clearfix::after {
            content: "";
            clear: both;
            display: table;
        }
        
        

        

        .project-1 {
            width: 900px;
            margin: 0 auto;

            .img-container {

                width: 100%;
                position: relative;
                margin-bottom: 30px;

                img {
                    display: block;
                    width: 100%;
                    height: auto;

                    -webkit-box-shadow: 0px 0px 44px 0px rgba(77,77,77,0.15);
                    -moz-box-shadow: 0px 0px 44px 0px rgba(77,77,77,0.15);
                    box-shadow: 0px 0px 44px 0px rgba(77,77,77,0.15);

                    // margin-bottom: 50px;
                }

                .overlay {
                    position: absolute;
                    
                    top: 0;
                    left: 0;
                    right: 0;
                    background-color: black;
                    opacity: 0;
                    overflow: hidden;
                    width: 100%;
                    height: 100%;
                    transition: .5s ease;

                    .text {
                        white-space: nowrap; 
                        color: white;
                        font-size: 20px;
                        position: absolute;
                        overflow: hidden;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                        -ms-transform: translate(-50%, -50%);
                    }
                    
                }

                &:hover .overlay {
                    transition: .5s;
                    opacity: 1;
                }

            }
        }
    }

    @media screen and (max-width: 1000px) {
        .projects {
            .project-1 {
                width: 700px;

                .project-title{
                    width: 300px;

                }

                .project-description {
                    width: 400px;
                }
            }
        }
    }

    @media screen and (max-width: 800px) {
        .projects {
            font-size: 0.9em;
            .project-1 {
                width: 600px;

                .project-title{
                    width: 600px;
                    margin-bottom: 50px;
                    button {
                        width: 200px;
                        margin-right: 40px;
                        line-height: 40px;
                    }
                }

                .project-description {
                    width: 600px;
                }
            }
        }
    }

    @media screen and (max-width: 700px) {
        .projects {
            .project-1 {
                width: 500px;
                
                .project-title{
                    width: 500px;
                    button {
                        margin-right: 30px;
                    }
                }

                .project-description {
                    width: 500px;
                }
            }
        }
    }

    @media screen and (max-width: 500px) {
        .projects {
            .project-1 {
                width: 90%;
                
                
                .project-title{
                    width: 90%;
                    margin-bottom: 30px;

                    button {
                        font-size: 0.8em;
                        width: 170px;
                        margin-right: 30px;

                        &:hover{

                        }
                    }
                }

                .project-description {
                    width: 90%;
                    margin-bottom: 0px;
                    font-size: 0.9em;
                }
            }
        }
    }



    
    
</style>

