<template>
    <div id="app">
        <NavBar />

        <Introduction v-bind:onClick="openContactForm"/>

        <Projects />

        <Skills />

        <Footer v-bind:onClick="openContactForm"/>

        <ContactForm v-bind:showContactForm="showContactForm" v-bind:onClick="closeContactForm"/>

    </div>
</template>

<script>
    import NavBar from './components/NavBar';
    import Introduction from './components/Introduction';
    import Projects from './components/Projects';
    import Skills from './components/Skills';
    import Footer from './components/Footer';
    import ContactForm from './components/ContactForm'

    export default {
        name: "App",
        components: {
            NavBar,
            Introduction,
            Projects,
            Skills,
            Footer,
            ContactForm
        },

        data() {
            return {
                showContactForm: false
            }
        },

        methods: {
            openContactForm () {
                this.showContactForm = true;
                console.log(this.showContactForm);
            },
            
            closeContactForm () {
                this.showContactForm = false;
                console.log(this.showContactForm);
            }
        }
    }

    
</script>

<style lang="scss">
    @import './scss/style.scss';


</style>
