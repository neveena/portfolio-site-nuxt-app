<template>
    <div>
        <nav-bar />
        <div id="nav-scroller">
            <banner id="home" />
            <about id="about" />
            <div id="portfolio" style="height: 500px;">
                <h2>Work</h2>
                <p>Most of my work was done as a part of a organisation which can't be shared publicily.</p>
                <p>
                    Hey there! Most of my work was done as a part of a organisation which can't be shared publicily 😞. Now, while this page is in the works, probably start with technologies used on my site.
                    This site is hosted on Netlify, uses Vue, NuxtJS, Bootstrap4 and Styled Components and the codebase is right on my GitHub neveenaferrao/personal-portfolio-site-nuxt-app.
                    You can also download a copy of resume or check out my GitHub.
                </p>
                <p>
                    If you're still not convinced or you're just curious about some of my other work and want to hire me, feel free to send me a mail and we can schedule a demo call for sometime where I'll show you the apps I've worked on.
                </p>
            </div>
            <div id="contact" style="height: 500px;">
                contact
            </div>
        </div>
    </div>
</template>

<script>
import NavBar from '~/components/Navbar';
import Banner from '~/components/Banner';
import About from '~/components/About';

export default {
    components: {
        NavBar,
        Banner,
        About
    },
    created() {
        this.$root.$on('bv::scrollspy::activate', this.onActivate);
    },
    methods: {
        onActivate(target) {
            // console.log('Received event: "bv::scrollspy::activate" for target ', target);
        }
    }
};
</script>

<style>
    #nav-scroller {
        position: relative;
        overflow-y: scroll;
        height: 100vh;
    }
</style>
