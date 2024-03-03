<script>
    import { onMount } from "svelte";

    let scroll;
    let servicesWrapper;
    let scrollDir;
    // let dots             = document.querySelectorAll('.dot');
    let sections         = document.querySelectorAll('.section');
    let sectionContainer = document.querySelector('.sections');
    let reachedTop = false;

    onMount(() => {
        sections         = document.querySelectorAll('.section');
        sectionContainer = document.querySelector('.sections');
    });

    let currentSection = 0;
    let canScroll = true;
    let touchStart = 0;
    let touchEnd = 0;

    // set event listeners on the dots
    // dots.forEach((dot, index) => {
    //     dot.addEventListener('click', (event) => {
    //         console.log(event)
    //         resetDotIndicator();
    //         currentSection = index;
    //         sectionContainer.style.top = (currentSection * -100) + 'vh';
    //         setDotIndicator();
    //     });
    // });

    const handleDotClick = e => {
        console.log(e.target.dataset.index);
        const index = e.target.dataset.index;
        currentSection = index;
        sectionContainer.style.top = (currentSection * -100) + 'vh';
    };

    document.addEventListener('touchstart', (event) => {
        touchStart = event.changedTouches[0].clientY;
    });

    document.addEventListener('touchend', (event) => {
        touchEnd = event.changedTouches[0].clientY;
        if (touchStart > touchEnd) {
            performScroll(1);
        } else {
            performScroll(-1);
        }
    });

    // Add event listener for scrolling, so we can do our scroll jacking
    document.addEventListener('wheel', (event) => {
        // Check if we can scroll yet, or if we're in the middle of a scroll jack.
        // If so, prevent all scrolling
        if (!canScroll) {
            return; 
        }
        
        // Not in a scroll, so set a timeout for when scrolling can happen next
        canScroll = false;
        setTimeout(() => {
            canScroll = true;
        }, 1000);
    
        // Perform the scroll to the next section
        // First, get the next section to scroll to by checking if the scroll position is greater or less than the position of the current position.
        scrollDir = event.deltaY > 1 ? 1 : -1;
        performScroll(scrollDir);
    });

    function performScroll(scrollDir) {
        if (reachedTop) {
           
            currentSection += scrollDir;
            
            // Make sure we stick to real sections and don't scroll out of it.
            if (currentSection >= sections.length - 1) {
                currentSection = sections.length - 1;
                
            }
            if (0 > currentSection) {
                currentSection = 0;
            }
            
            // perform the 'scroll'
            sectionContainer.style.top = (currentSection * -100) + 'vh'; 
        }
    }

    // $: console.log(scroll);
    // $: console.log(servicesWrapper?.offsetTop);
    $: if (scroll) {
        if (scroll >= servicesWrapper?.offsetTop && scroll < servicesWrapper.clientHeight) {
            reachedTop = true;
        } else {
            reachedTop = false;
        }
    }
</script>

<svelte:window bind:scrollY={scroll} />

<div class="services-wrapper" bind:this={servicesWrapper}>
    <section class="services" class:fixed={reachedTop} translate="no" data-new-gr-c-s-check-loaded="14.1157.0" data-gr-ext-installed="">
    <div class="navigation">
        <button class="dot" class:current-dot={currentSection == 0} on:click={handleDotClick} data-index="0"></button>
        <button class="dot" class:current-dot={currentSection == 1} on:click={handleDotClick} data-index="1"></button>
        <button class="dot" class:current-dot={currentSection == 2} on:click={handleDotClick} data-index="2"></button>
        <button class="dot" class:current-dot={currentSection == 3} on:click={handleDotClick} data-index="3"></button>
        <button class="dot" class:current-dot={currentSection == 4} on:click={handleDotClick} data-index="4"></button>
    </div>
    <div class="sections" style="top: -100vh;">
        <div class="section" data-index="0">
            <h2>Section: 1</h2>
            <p>Tail laborum venison, tempor chislic t-bone turkey qui eu short ribs. Corned beef velit lorem strip steak, consequat dolore ball tip nisi nostrud. In consectetur consequat, meatloaf cow dolore shoulder nostrud ullamco jerky est kevin in. Chuck andouille sunt officia tenderloin sint duis boudin nisi shank kielbasa ut dolore.</p>
        </div>
        <div class="section" data-index="1">
            <h2>Section: 2</h2>
            <p>Drumstick sint do shoulder nostrud, anim eu strip steak aliqua rump quis. Tri-tip proident ut ribeye magna consequat. Chuck officia laborum chicken, shank magna swine sausage t-bone. Beef ribs chislic incididunt short ribs beef sunt.</p>
        </div>
        <div class="section" data-index="2">
            <h2>Section: 3</h2>
            <p>Kielbasa ham anim, turducken biltong ex pork loin. Deserunt ribeye dolore, elit sint anim tempor bacon. Tongue cupidatat nostrud hamburger. Ea kielbasa shankle chuck est, picanha esse minim bresaola mollit exercitation landjaeger shank doner non.</p>
        </div>
        <div class="section" data-index="3">
            <h2>Section: 4</h2>
            <p>Swine chicken reprehenderit dolor, salami esse sausage voluptate biltong. Ut duis strip steak adipisicing pork meatball sausage et. Eiusmod hamburger ground round, nostrud beef ribs in dolore ribeye sed shank veniam cupidatat biltong sausage. Picanha tail sint pancetta ground round chuck.</p>
        </div>
        <div class="section" data-index="4">
            <h2>Section: 5</h2>
            <p>Corned beef jerky turducken in, ribeye chislic ham hock ut flank. Et sausage prosciutto quis, strip steak andouille dolor rump cupim. Pariatur elit kevin, sunt eu ribeye shankle enim pastrami proident pig aute tempor ea. Shank strip steak short loin dolore pig voluptate excepteur sirloin irure, aliquip pastrami.</p>
        </div>
    </div>
    </section>
</div>      

<style lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Roboto');

    .services-wrapper {
        width: 100%;
        height: 100vh;
    }
    .services {
        position: relative;
        overflow: hidden;
        height: 100vh;
        width: 100%;
        background-color: #333;
        overscroll-behavior: contain;

        &.fixed {
            position: fixed;
            top: 0;
            left: 0;
            z-index: 10;
        }
    }

    h2 {
        text-align: center;
        margin-bottom: 20px;
    }

    .navigation {
        position: absolute;
        top: 10%;
        left: 5%;
        border: 2px solid #FFF;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        z-index: 10;
        
        .dot {
            margin: 5px;
            height: 10px;
            width: 10px;
            border-radius: 100%;
            background-color: #FFF;
            cursor: pointer;
            z-index: 10;
            
            &.current-dot {
            background-color: #5bFFEE;  
            }
        }
    }

    .sections {
        position: relative;
        top: 0;
        transition: top 1s ease;
        color: #FFF;
    }

    .section {
        margin: auto;
        padding: 0 calc(6% + 30px);
        max-width: 800px;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        
        & p {
            line-height: 1.4;
        }
    }

    // Loader Styles
    @mixin make-circle($dim, $time, $color, $dir) {
        height: $dim * 1px;
        width: $dim * 1px;
        top: calc(((90 - $dim) / 2) * 1px);
        left: calc(((90 - $dim) / 2) * 1px);
        border-top: 5px solid $color;
        animation: menu-spinner $time infinite linear;
        animation-direction: $dir;
    }

    .loader {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: 75px;
        width: 75px;
        
        .circle {
            position: absolute;
            border: 5px solid #333;
            border-radius: 100%;
        }
        
        .circle0 {
            @include make-circle(100, 1.5s, #FFF, forward);
        }
        .circle1 {
            @include make-circle(80, 1s, #FFF, reverse);
        }
        .circle2 {
            @include make-circle(60, .8s, #FFF, forward);
        }
        .circle3 {
            @include make-circle(40, .62s, #FFF, reverse);
        }
        .circle4 {
            @include make-circle(20, .43s, #FFF, forward);
        }
    }

    @keyframes menu-spinner {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>