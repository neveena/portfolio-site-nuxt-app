<template>
    <section>
        <div class="container">
            <h2>Contact me</h2>
            <blockquote>
                "Any fool can write code that a computer can understand. Good programmers write code that humans can understand."
                <small><i>~ Martin Fowler</i></small>
            </blockquote>
            <form name="contact" method="post" netlify netlify-honeypot="bot-field">
                <div class="form-row">
                    <div class="form-group col-md-6">
                        <label for="fullname">Full name</label>
                        <input id="fullname" type="text" name="name" placeholder="Full name" class="form-control">
                    </div>
                    <div class="form-group col-md-6">
                        <label for="email">Email</label>
                        <input id="email" type="email" name="email" placeholder="Email" class="form-control">
                    </div>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" placeholder="Message" rows="5" class="form-control" />
                </div>
                <button type="submit" class="btn">
                    <div class="btn-custom">
                        Send
                    </div>
                </button>
            </form>
        </div>
        <footer-nav />
    </section>
</template>

<script>
import FooterNav from './Footer';
export default {
    name: 'Contact',

    components: {
        FooterNav
    }
};
</script>

<style lang="scss" scoped>
    section {
        padding: 100px 0 0;
        text-align: center;
        background-color: $primary;
        min-height: 100vh;

        h2 {
            color: $headings;

            @include media-breakpoint-up(md) {
                margin-bottom: 20px;
            }

            span {
                font-weight: 700;
            }
        }
    }

    blockquote {
        color: #ffffff;
        max-width: 700px;
        margin: 0 auto;
        font-size: 17px;
    }

    small {
        display: block;
        font-size: 15px;
    }

    form {
        text-align: left;
        color: #ffffff;
        max-width: 800px;
        margin: 30px auto;
    }

    label {
        font-size: 20px;
    }

    button {
        position: relative;
        overflow: hidden;
        z-index: 1;
        padding: 0;
        margin: 20px 0 0 auto;
        display: block;
    }

    .btn-custom {
        padding: 15px;
        width: 200px;
    }
</style>
