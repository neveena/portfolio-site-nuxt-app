<template>
    <section>
        <div class="container">
            <h2>Hello <span class="wave">👋</span></h2>
            <h2>
                <span class="title" />
            </h2>
            <blockquote>
                <p>
                    "Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live."
                </p>
                <small>  — John F. Woods</small>
            </blockquote>
            <button class="btn">
                <div class="btn-custom">
                    Download Resume
                </div>
            </button>
        </div>
    </section>
</template>

<script>
import Typed from 'typed.js';

export default {
    name: 'Banner',

    mounted() {
        const options = {
            strings: ['My name is Neveena Ferrao', 'I\'m a Frontend Developer.'],
            typeSpeed: 50
        };
        if (process.browser) {
            this.$nextTick(() => {
                /* eslint-disable no-unused-vars */
                const typed = new Typed('.title', options);
            });
        }
    }
};
</script>
<style>
    .typed-cursor {
        font-size: 40px;
    }

    .typed-cursor.typed-cursor--blink {
        opacity: 0;
    }
</style>
<style lang="scss" scoped>
    section {
        position: relative;
        padding: 90px 0;
        text-align: center;
        min-height: 100vh;
        display: flex;
        align-items: center;
        background-color: $primary;
        color: #ffffff;

        h2 {
            font-size: 40px;
        }
    }

    .container {
        position: relative;
        z-index: 1;
    }
    .title {
        font-size: 55px;
        color: $headings;
    }

    span.wave {
        animation-name: wave-animation;
        animation-duration: 2.5s;
        animation-iteration-count: infinite;
        transform-origin: 70% 70%;
        display: inline-block;
    }

    @keyframes wave-animation {
        0% { transform: rotate(  0.0deg) }
        10% { transform: rotate(-10.0deg) }
        20% { transform: rotate( 12.0deg) }
        30% { transform: rotate(-10.0deg) }
        40% { transform: rotate(  9.0deg) }
        50% { transform: rotate(  0.0deg) }
        100% { transform: rotate(  0.0deg) }
    }

    blockquote {
        max-width: 500px;
        margin: 1.2rem auto;
        p {
            margin-bottom: 0.5rem;
        }
    }

    button {
        margin-top: 30px;
        position: relative;
        overflow: hidden;
        z-index: 1;
        padding: 0;
    }
</style>
