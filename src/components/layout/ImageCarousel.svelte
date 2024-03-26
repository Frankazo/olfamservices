<script>
    import { imagesArray } from "../../constants/services";
    import RightArrow from "../../assets/RightArrow.svelte";
    import LeftArrow from "../../assets/LeftArrow.svelte";
    
    let currentIndex = 0;
    $: current = imagesArray[currentIndex];

    const handleNext = () => {
        if (currentIndex + 1 > imagesArray.length - 1) {
            currentIndex = 0;
        } else {
            currentIndex += 1;
        }
    };

    const handlePrev = () => {
        if (currentIndex - 1 < 0) {
            currentIndex = imagesArray.length - 1;
        } else {
            currentIndex -= 1;
        }
    };
</script>

<div class="imgCarousel">
    <div class="imageWrapper" style="background-image: url({current.img})">
        <!-- <img src="{current.img}" alt="service"> -->
    </div>
    <div class="arrows">
        <button on:click={handlePrev}><LeftArrow /></button>
        <button on:click={handleNext}><RightArrow /></button>
    </div>
</div>

<style lang="scss">
    .imgCarousel {
        padding: 100px 0;
            display: flex;
            justify-content: center;

        .imageWrapper {
            height: 90vh;
            width: 80vw;
            max-height: 1200px;
            max-width: 2200px;
            background-size: cover;
            background-position: center;
            -webkit-transition: all .3s ease-in-out;
            -moz-transition: all .3s ease-in-out;
            transition: all .3s ease-in-out;
        }

        .arrows {
            position: absolute;
            top: 50%;
            padding: 0 50px;
            display: flex;
            width: 100%;
            justify-content: space-between;
            z-index: 2;

            button {
                width: 40px;
                height: 40px;
                transition: scale 0.25s;
            }

            button:active {
                scale: 0.8;
            }

            button:focus {
                outline:0;
            }
        }

        @media only screen and (max-width: 767px) {
            .imageWrapper {
                height: 80vh;
                width: 90%;
            }

            .arrows {
                padding: 0 5px;
            }
        }
    }
</style>