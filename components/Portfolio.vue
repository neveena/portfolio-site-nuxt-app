<template>
    <section class="portfolio">
        <div class="container">
            <h2>My <strong>work</strong></h2>
            <p>
                Most of my work was done as a part of a organisation which can't be shared publicily 😞. Now, while this page is in the works, probably start with technologies used on this site.
                This site is hosted on Netlify, NuxtJS(Vue Framework) and Bootstrap4 (Scss). The codebase is on my GitHub <a href="https://github.com/neveena/portfolio-site-nuxt-app" target="_blank" rel="external">neveenaferrao/portfolio-site-nuxt-app</a>.
                You can also <a href="/Neveena-Frontend_Developer.pdf" download>download</a> a copy of resume or check out my <a href="https://github.com/neveena" target="_blank" rel="external">GitHub</a> for other projects.
            </p>
            <p>
                If you're still not convinced or you're just curious about some of my other work, feel free to send me a mail at <a href="mailto:neveena.praveen@gmail.com">neveena.praveen@gmail.com</a>.
            </p>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Portfolio'
};
</script>

<style lang="scss" scoped>
    .portfolio {
        background-color: $secondary;
        padding: 70px 0;
        display: flex;
        align-items: center;
        @include media-breakpoint-up(md) {
            min-height: 100vh;
        }
    }

    h2 {
        color: $primary;

        @include media-breakpoint-up(md) {
            margin-bottom: 30px;
        }
    }

    p {
        font-size: 17px;
        @include media-breakpoint-up(md) {
            font-size: 22px;
        }
    }

    a {
        font-weight: 600;
        text-decoration: underline;
    }
</style>
