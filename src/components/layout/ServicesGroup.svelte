<script>
    import { servicesArray } from "../../constants/services";
    import ServiceCard from "../shared/ServiceCard.svelte";
</script>


<section class="services">
    <div class="services__container">
        <div class="services__content">
            <div class="h2">The all-in-one solution for civil projects</div>

            <div class="ctaBtn"><a class="button" href="#about">About OLFAM</a></div>
        </div>

        <div class="services__cards">
            {#each servicesArray as service}
                <ServiceCard {service} />
            {/each}
        </div>
    </div>
</section>

<style lang="scss">
    .services {
        background-color: #fff;

        &__container {
            padding: 120px 0;
            width: 100%;
            max-width: 1600px;
            margin: 0 auto;
        }

        &__content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: #000;
            z-index: 5;
            height: fit-content;
            width: 100%;
            margin-bottom: 75px;

            .h2 {
                max-width: 900px;
                // font-size: clamp(2.5rem, 5vw, 5rem);
                font-weight: 600;
                letter-spacing: -3px;
            }
        }

        &__cards {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 40px;
        }

        @media screen and (max-width: 1024px) {
            &__container {
                padding: 100px 20px;
            }
        }

        @media screen and (max-width: 767px) {
            &__container {
                flex-direction: column;
            }

            &__content {
                padding: 0;
                flex-direction: column;
                align-items: flex-start;
                width: 100%;

                .h2 {
                    margin-bottom: 50px;
                }
            }

            &__cards {
                grid-template-columns: 1fr;
            }
        }
}
</style>