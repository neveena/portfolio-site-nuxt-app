<template>
    <div class="about">
        <div class="container">
            <h2><span>About</span> me</h2>
            <p>
                Over the past 5 years, I've built products for companies and businesses around the globe ranging from basic websites to complex solutions apps with focus on fast, elegant and accessible user experiences.
                Most recently, I was a front end developer with <a href="http://netsells.co.uk/" rel="">Netsells Ltd</a>, building multiple Vue.js based applications for organisation and individuals.
                Before that, I was a Web developer at Four Clover Reality Private Ltd, building multiple microsites, landing pages and internal CRM.
            </p>
            <p>
                I'm now available for contracts and remote full-time roles.
            </p>
            <button class="btn">
                <div class="btn-custom">
                    Hire me
                </div>
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'About'
};
</script>

<style lang="scss" scoped>
    .about {
        padding: 130px 0;
        text-align: center;
        // background-color: #f9f9f9;

        h2 {
            color: $primary;
            margin-bottom: 30px;
            span {
                font-weight: 700;
            }
        }

        p {
            font-size: 20px;
            color: #363636;
            max-width: 800px;
            margin: 0 auto;
        }

        button {
            margin-top: 30px;
            position: relative;
            overflow: hidden;
            z-index: 1;
            padding: 0;
        }
    }
</style>
