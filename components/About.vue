<template>
    <section class="about">
        <div class="container">
            <h2>A little <span>about me</span></h2>
            <p>
                I have been developing websites professionally for over 5 years. I've built products for companies and businesses around the globe ranging from basic websites to complex solutions apps with focus on fast, elegant and accessible user experiences.
                Most recently, I was a front end developer with <a href="http://netsells.co.uk/" rel="external nofollow noreferrer" target="_blank">Netsells Ltd</a>, building multiple Vue.js based applications for organisation and individuals.
                Before that, I was a Web developer at <a href="http://www.clovermark.in/" rel="external nofollow noreferrer" target="_blank">Four Clover Reality Private Ltd</a>, building microsites, landing pages and internal CRM.
            </p>
            <p>
                I enjoy pushing the limits of the browser, solving difficult problems, and making usable applications. Highly self-motivated, goal-oriented with a quest and deal to learn new technologies. I always believes in innovation, passion and success.
            </p>
            <a href="https://www.linkedin.com/in/neveenaferrao/" target="_blank" rel="external nofollow noreferrer" class="btn btn-link">
                <div class="btn-custom">
                    Connect with me <strong>LinkedIn</strong>
                </div>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'About'
};
</script>

<style lang="scss" scoped>
    // Colors
    $bg-color: #f7f7f7;
    $dot-color: rgba(61, 25, 94, 0.25);

    .about {
        padding: 50px 0;
        display: flex;
        align-items: center;
        background: linear-gradient(90deg, #f7f7f7 20px, transparent 1%) center, linear-gradient(#f7f7f7 20px, transparent 1%) center, rgba(61, 25, 94, 0.1);
        background-size: 22px 22px;

        @include media-breakpoint-up(md) {
            padding: 80px 0;
            background: linear-gradient(90deg, $bg-color (22px - 2px), transparent 1%) center, linear-gradient($bg-color (22px - 2px), transparent 1%) center, $dot-color;
            background-size: 22px 22px;
            min-height: 100vh;
        }

        h2 {
            color: $primary;

            @include media-breakpoint-up(md) {
                margin-bottom: 30px;
            }

            span {
                font-weight: 700;
            }
        }

        p {
            font-size: 16px;
            color: #474747;

            @include media-breakpoint-up(md) {
                font-size: 22px;
            }

            a {
                font-weight: 700;
                text-decoration: underline;

                &:hover {
                    color: #607D8B;
                }
            }
        }
    }

    .btn-link {
        position: relative;
        overflow: hidden;
        z-index: 1;
        padding: 0;
        font-weight: 500;
        font-size: 15px;
        text-decoration: none;

        @include media-breakpoint-up(md) {
            font-size: 20px;
            margin-top: 30px;
        }
    }

    .btn-custom {
        border-color: $primary;
        color: $primary;
        background-color: $secondary;

        &:before {
            background-color: $primary;
        }

        &:hover {
            color: $secondary;
            background-color: transparent;
            &:before {
                transform: translateX(0px);
                border-color: $primary;
            }
        }
    }
</style>
