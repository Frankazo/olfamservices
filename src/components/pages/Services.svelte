<script>
    import Banner from '../layout/Banner.svelte';
    import ServicesGroup from '../layout/ServicesGroup.svelte';
</script>

<div class="projects">
    <div class="projects__content">
        <div class="projects__header">
            <h1>Our Services</h1>
            <p>Request Your Quote Today and Build with Confidence!</p>
            <div class="cta">
               <a href="#contact" class="button">Request a Quote</a>
            </div>
        </div>
        <ServicesGroup />
    </div>
    <Banner />
</div>

<style lang="scss">
    .projects {
        &__content {
            padding: 100px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            color: #000;
        }

        &__header {
            width: 100%;
            height: 50vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #000;
            margin: auto;
            z-index: 10;

            h1 {
                font-weight: bold;
                font-style: italic;
            }

            p {
                font-size: clamp(0.8rem, 3vw, 1.3rem);
            }

            .cta {
                display: flex;
                gap: 20px;
                margin-top: 50px;
            }
        }
    }
</style>