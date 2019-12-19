<template>
    <div>
        <nav-bar />
        <div id="nav-scroller" class="main">
            <banner id="home" />
            <about id="about" />
            <portfolio id="portfolio" />
            <contact id="contact" />
        </div>
    </div>
</template>

<script>
import NavBar from '~/components/NavBar';
import Banner from '~/components/Banner';
import About from '~/components/About';
import Portfolio from '~/components/Portfolio';
import Contact from '~/components/Contact';

export default {
    components: {
        NavBar,
        Banner,
        About,
        Portfolio,
        Contact
    },

    mounted() {
        /* eslint-disable */
        onePageScroll('.main', {
            sectionContainer: 'section',
            easing: 'ease',
            animationTime: 1000,
            pagination: true,
            updateURL: false,
            beforeMove: (index) => {},
            afterMove: (index) => {
                this.$store.commit('navigation/setCurrentSection', parseInt(index));
            },
            loop: false,
            keyboard: true,
            responsiveFallback: 767
        });
    },
};
</script>

