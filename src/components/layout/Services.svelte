<script>
    const servicesArray = [
        {
            id: 'service1',
            name: 'Framing',
            img: 'images/framing.jpg',
            description: 'Our framing service lays the foundation for every successful construction project. With precision and expertise, our team skillfully constructs the skeletal structure of your building, ensuring it meets the highest industry standards. From residential homes to commercial spaces, our framing services provide the sturdy framework upon which your vision is built.'
        },
        {
            id: 'service2',
            name: 'Roofing',
            img: 'images/Roofing.jpg',
            description: "Elevate your property's protection and aesthetics with our roofing services. Our experienced roofers specialize in installing durable and weather-resistant roofing materials. Whether it's a repair, replacement, or new installation, we prioritize quality craftsmanship to safeguard your investment against the elements while enhancing the overall curb appeal of your structure."
        },
        {
            id: 'service3',
            name: 'Wood and Metal',
            img: 'images/wood&metal.jpg',
            description: "Our wood and metal services bring versatility and durability to your construction project. From crafting custom woodwork to precision metal fabrication, our skilled artisans ensure that every detail aligns with your design vision. Enhance the beauty and functionality of your space with our expertly crafted wood and metal solutions, tailored to your unique needs."
        },
        {
            id: 'service4',
            name: 'Windows',
            img: 'images/window.jpg',
            description: "Welcome natural light and elevate your interior with our professional window installation services. We specialize in the precise fitting and installation of a wide range of window types. Our team ensures energy efficiency, security, and aesthetic appeal, transforming your space with well-crafted windows that not only complement your design but also contribute to a comfortable and inviting atmosphere."
        },
        {
            id: 'service5',
            name: 'Doors',
            img: 'images/door.jpg',
            description: "Make a grand entrance with our door installation services. From stylish front doors to functional interior doors, we specialize in seamless installations that enhance both security and aesthetics. Our skilled craftsmen pay meticulous attention to detail, ensuring a perfect fit for every door. Elevate the overall appeal of your property while maintaining the highest standards of quality and durability."
        },
    ];
    let current = servicesArray[0];
</script>

<section id="services" class="services">
    <div class="services__nav">
        <div class="mobileAssets">
            <div class='asset' style="background-image: url({current.img})"></div>
        </div>
        {#each servicesArray as service}
            <button class:current={current.id == service.id} on:click={() => current = service}>{service.name}</button>
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
            justify-content: center;
            padding: 50px;
            z-index: 10;

            button {
                color: #929292;
                font-size: clamp(3rem, 5vw, 5rem);
                font-weight: 600;
                text-transform: uppercase;
                outline: none;
                text-align: left;
                text-wrap: nowrap;

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