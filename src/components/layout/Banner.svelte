<section class="banner">
    <div class="banner__slide" style="background-image: url(images/services/framing/023.jpeg)">
        <div class="banner__slide__content wrapper">
            <h2 class="h2">Connect Now for a Constructive Tomorrow.</h2>

            <div class="banner__slide__content__copy">
                <p>Embark on a Building Journey. Reach Out Today.</p>

                <a class="button button--white " href="#contact">Contact Us</a>
            </div>
        </div>
    </div>
    <div class="overlay"></div>
</section>

<style lang="scss">
    .banner {
        background-color: #fff;

        .banner__slide {
            display: flex;
            justify-content: center;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            max-height: 720px;
            width: 100%;
            color: #fff;
            
            &__content {
                width: 100%;
                display: flex;
                align-items: flex-start;
                flex-direction: column;
                justify-content: flex-end;
                gap: 100px;
                padding: 0;
                max-width: 1600px;
                margin: 100px 0;
                z-index: 10;

                h2 {
                    text-align: left;
                    font-size: clamp(2.5rem, 5vw, 5rem);
                    font-weight: 600;
                    letter-spacing: -3px;
                    width: 70%;
                }

                &__copy {
                    display: flex;
                    width: 100%;
                    justify-content: space-between;
                    align-items: flex-start;

                    p {
                        max-width: 70%;
                        font-size: 1.875rem;
                        font-weight: 200;
                        line-height: 40px;
                    }
                }
            }
        }

        @media screen and (max-width: 767px) {

            .banner__slide {
                &__content {
                    padding: 0 20px;
                    gap: 10px;
                    margin: 50px 0;


                    h2 {
                        width: auto;
                    }

                    &__copy {
                        gap: 20px;
                        flex-direction: column;

                        p {
                            max-width: none;
                        }
                    }
                }
            }
        }
    }

</style>