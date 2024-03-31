<script>
    // Svelte
    import { onMount } from 'svelte';
    import { servicesArray } from '../../constants/services';
    import Banner from '../layout/Banner.svelte';
    import ImageGrid from '../layout/ImageGrid.svelte';
    let currentService;

    onMount(() => {
        const urlParams = new URLSearchParams(window.location.search);
        const serviceId = urlParams.get('id');
        currentService = servicesArray.find(service => service.id == serviceId);
    });
</script>

{#if currentService}
    <div class="service">
        <div class="service__content">
            <div class="service__header">
                <h1>{currentService.name}</h1>
                <p>Request Your Quote Today and Build with Confidence!</p>
                <div class="cta">
                    <a href="#contact" class="button">Request a Quote</a>
                </div>
            </div>

            <div class="service__description">
                <h2>About {currentService.name}</h2>
                <div class="divider"></div>
                <p>{currentService.description}</p>
            </div>

            {#if currentService.images}
                <ImageGrid {currentService}/>
            {/if}
        </div>


        <Banner />
    </div>
{/if}

<style lang="scss">
    .service {
        &__content {
            padding: 100px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            color: #000;
        }


        &__header {
            max-width: 1600px;
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


        &__description {
            display: flex;
            flex-direction: column;
            justify-content: center;
            max-width: 1600px;
            gap: 20px;

            p {
                font-size: clamp(0.8rem, 3vw, 1.5rem);
            }
        }


        @media only screen and (max-width: 767px) {
            
            &__description {
                padding: 0 20px;
            }
        }
    }
</style>