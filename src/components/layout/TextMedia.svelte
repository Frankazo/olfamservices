<section class="text-media">
    <div class="text-media__container">
        <div class="text-media__asset" style="background-image: url(images/about-cropped.jpeg);">
        </div>
        
        <div class="text-media__content">
            <div class="h2">OLFAM Services: Your Best Construction Partner in the South of Florida!</div>
            <p>Founded by 2 visionary engineers, Francisco and Pedro, with a passion for building Florida's future."</p>

            <div class="ctaBtn"><a class="button" href="#about">About OLFAM</a></div>
        </div>
    </div>
</section>

<style lang="scss">
    .text-media {
        background-color: #fff;

        &__container {
            display: flex;
            justify-content: center;
            align-items: flex-start;
            padding: 120px 0;
            width: 100%;
            max-width: 1600px;
            margin: 0 auto;
        }

        &__asset {
            height: 100%;
            width: 100%;
            min-height: 800px;
            max-width: 600px;
            background-position: center;
            background-size: cover;
        }

        &__content {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            color: #000;
            z-index: 5;
            padding: 0 75px;
            height: fit-content;
            width: 60%;

            .h2 {
                margin-bottom: 100px;
                font-size: clamp(2rem, 5vw, 5rem);
                font-weight: 600;
                letter-spacing: -3px;
            }

            p {
                font-size: clamp(1.2rem, 3.5vw, 1.875rem);
                font-weight: 200;
                line-height: 40px;
            }
        }

        .ctaBtn {
            margin-top: 100px;
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

            &__asset {
                height: 200px;
                min-height: 0;
            }

            &__content {
                padding: 0;
                width: 100%;

                .h2 {
                    margin-bottom: 25px;
                }

                p {
                    line-height: 30px;
                }
            }


            .ctaBtn {
                margin-top: 50px;
            }
        }
}
</style>