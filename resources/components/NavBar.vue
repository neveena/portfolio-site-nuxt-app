<template>
    <header :class="{ scroll: scrolled }">
        <div class="container">
            <b-navbar v-b-scrollspy="options" toggleable="lg" type="dark">
                <b-navbar-brand tag="h1" class="mb-0">
                    Neveena
                </b-navbar-brand>
                <a type="button" aria-haspopup="menu" aria-label="Open menu" class="hamburger_menu" />
                <!-- <b-navbar-nav class="ml-auto">
                    <b-nav-item href="#home">
                        Home
                    </b-nav-item>
                    <b-nav-item href="#about">
                        About
                    </b-nav-item>
                    <b-nav-item href="#portfolio">
                        Portfolio
                    </b-nav-item>
                    <b-nav-item href="#contact">
                        Contact us
                    </b-nav-item>
                </b-navbar-nav> -->
            </b-navbar>
        </div>
    </header>
</template>

<script>
export default {
    name: 'NavBar',

    data() {
        return {
            status: {
                scroll: false
            },
            options: {
                element: '#nav-scroller',
                offset: 70,
                method: 'position'
            }
        };
    },

    computed: {
        scrolled() {
            return this.status.scroll;
        }
    },

    mounted() {
        const el = document.querySelector('#nav-scroller');
        el.addEventListener('scroll', () => {
            if (el.scrollTop < 20) {
                this.status.scroll = false;
                return;
            }

            this.status.scroll = true;
        });
    }
};
</script>

<style lang="scss" scoped>
    header {
        position: fixed;
        width: 100%;
        top: 0;
        z-index: 6;

        // &.scroll {
        //     box-shadow: 0 1px 8px 3px rgba(0, 0, 0, 0.050980392156862744);
        //     background-color: #ffffff;

        //     .navbar-dark .navbar-nav .nav-link {
        //         color: $primary;
        //         font-size: 18px;
        //     }

        //     .navbar h1 {
        //         color: $primary;
        //         font-size: 27px;
        //     }

        //     .hamburger_menu {
        //         &:before,
        //         &:after {
        //             background-color: $primary;
        //         }
        //     }
        // }
    }
    @include media-breakpoint-up(md) {
        .viewing-page-2,
        .viewing-page-3,
        .viewing-page-5 header {
            //top: 100%;

            .navbar-brand {
                color: $primary;
            }
            .hamburger_menu {
                &:before,
                &:after {
                    background-color: $primary;
                }
            }
        }
    }

    header .navbar  {
        padding: 0.5rem 0rem;
        justify-content: space-between;
        h1 {
            font-size: 35px;
            font-weight: 700;
            color: $headings;
            letter-spacing: 1px;
        }
    }

    // .navbar-dark .navbar-nav .nav-link {
    //     color: #ffffff;
    //     font-size: 20px;
    //     padding-right: 0.8rem;
    //     padding-left: 0.8rem;
    //     &.active {
    //         color: #3d195f;
    //     }
    // }
    // .nav-item.active {
    //     //color: $primary;
    // }

    .hamburger_menu {
        position: relative;
        display: block;
        height: 22px;
        width: 85px;
        cursor: pointer;

        &:before,
        &:after {
            content: '';
            width: 58px;
            height: 3px;
            //right: 30px;
            position: absolute;
            transition: 0.2s ease;
            transform: rotate(0deg);
            background-color: $headings;
        }

        &:before {
            top: 0;
        }
        &:after {
            width: 42px;
            top: 1em;
        }
    }
</style>
