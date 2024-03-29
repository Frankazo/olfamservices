<script>
    export let service;
</script>

<div class="serviceCard">
    <div class="serviceCard__image" style="background-image: url({service.img});"></div>
    <div class="serviceCard__copy">
        <h3>{service.name}</h3>
        <p>{service.description}</p>
        <a href="#home">Learn More</a>
    </div>

</div>

<style lang="scss">
    .serviceCard {
        color: #000;
        margin-bottom: 50px;

        &__image {
            height: 400px;
            background-size: cover;
            background-position: center;
        }

        &__copy {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            gap: 20px;

            h3 {
                margin-top: 20px;
                font-size: clamp(1.5rem, 3.5vw, 2.1875rem);
            }

            p {
                font-size: clamp(1.2rem, 3.5vw, 1.5rem);
                line-height: 30px;
            }

            a {
                font-size: 1.5rem;
                color: #000;
                border-bottom: 1px solid #000;
                transition: border-bottom 0.1s;

                &:hover {
                    color: #000;
                    text-decoration: none;
                    border-bottom: 3px solid #000;
                }
            }
        }


        @media screen and (max-width: 767px) {

            &__image {
                height: 300px;
            }
        }

    }
</style>