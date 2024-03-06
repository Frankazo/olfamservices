<script>
    import { servicesArray } from "../../constants/services";
    let current = servicesArray[0];
</script>

<section id="services" class="services">
    <div class="services__nav">
        <div class="mobileAssets">
            <div class='asset' style="background-image: url({current.img})"></div>
        </div>
        {#each servicesArray as service}
            <button class:current={current.id == service.id} on:click={() => current = service} on:mouseenter={() => current = service}>{service.name}</button>
        {/each}
        <div class="divider"></div>
        <div class="description">
           <p>{current.description}</p> 
        </div>
    </div>

    <div class="services__assets">
        <div class='asset' style="background-image: url({current.img})"></div>
    </div>
</section>

<style lang="scss">
    .services {
        width: 100%;
        background-color: #fff;
        height: 100vh;

        &__nav {
            background-color: #fff;
            position: absolute;
            left: 0;
            width: 50%;
            height: 100vh;
            min-width: 550px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
            padding: 50px;
            z-index: 10;

            button {
                color: #929292;
                font-size: clamp(3rem, 5vw, 4rem);
                font-weight: 600;
                text-transform: uppercase;
                outline: none;
                text-align: left;
                text-wrap: nowrap;
                transition: color 1s;

                &.current {
                    color: #000;
                }
            }

            .divider {
                margin-top: 50px;
            }

            .description {
                p {
                    color: #000;
                    padding-top: 40px;
                    font-size: 24px;
                }
            }

            .mobileAssets {
                display: none;
                width: 100%;
                height: 300px;
                z-index: 1000;

                .asset {
                    width: 100%;
                    height: 100%;
                    background-size: cover;
                }
            }
        }

        &__assets {
            width: 100%;
            height: 100%;
            background-color: #000;

            .asset {
                background-position: center;
                background-size: cover;
                height: 100%;
                width: 50%;
                margin-left: auto;
                -webkit-transition: background-image 0.5s;
                transition: background-image 0.5s;
            }
        }

        @media screen and (max-width: 767px) {
            height: auto;

            &__assets {
                display: none;
            }

            &__nav {
                position: relative;
                height: auto;
                width: 100%;
                padding: 0;
                height: auto;
                gap: 10px;
                min-width: 0;

                .mobileAssets {
                    display: block;
                }

                button {
                    padding-left: 20px;
                    font-size: 1.5rem;
                }

                .divider {
                    margin-left: 20px;
                    margin-top: 15px;
                    height: 4px;
                    width: 50px;
                }

                .description p {
                    padding: 20px;
                    font-size: 16px;
                }


            }
        }
    }
</style>