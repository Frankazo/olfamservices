<script>
    export let scroll;
    let scrollTop = 0;
    let scrollState = '';
    let burguer = false;

    const handleScroll = () => {
        if (scroll > 80 && !burguer) {
            scrollState = scroll > scrollTop ? 'scrolling' : 'scrolling up';
        } else {
            scrollState = '';
        }

        scrollTop = scroll;
    };
</script>
<svelte:window on:scroll={handleScroll}/>

<header class="header {scrollState}" id="header" >
    <nav class="navbar container">
       <a href="#top" class="brand">Olfam Services</a>
       <!-- svelte-ignore a11y-click-events-have-key-events -->
       <!-- svelte-ignore a11y-no-static-element-interactions -->
       <div class="burger" id="burger" class:active={burguer} on:click={() => burguer = !burguer}>
          <span class="burger-line"></span>
          <span class="burger-line"></span>
          <span class="burger-line"></span>
       </div>
       <div class="menu" id="menu" class:active={burguer}>
          <ul class="menu-inner">
             <li class="menu-item"><a href="#top" class="menu-link" on:click={() => burguer = false}>Home</a></li>
             <li class="menu-item"><a href="#services" class="menu-link" on:click={() => burguer = false}>Services</a></li>
             <!-- <li class="menu-item"><a href="#projects" class="menu-link" on:click={() => burguer = false}>Projects</a></li> -->
             <!-- <li class="menu-item"><a href="#" class="menu-link">Contact</a></li> -->
          </ul>
       </div>
       <a href="#contact" class="menu-block" on:click={() => burguer = false}>Contact</a>
    </nav>
 </header>

<style lang="scss">
    // Header Section
    .header {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 100;
        width: 100%;
        height: auto;
        margin: 0 auto;
        transition: all 0.35s ease;
        background-color: rgba(0, 0, 0, 0.9);
        // background: var(--color-black-300);

        &.scrolling {
            transform: translateY(-100%);
            background: var(--color-black-300);
            box-shadow: var(--shadow-medium);
            
            &.up {
                background-color: rgba(0, 0, 0, 0.9);
                transform: translateY(0);
                transition: all .3s ease-out;
            }
        }
    }

    .navbar {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        column-gap: 1.25rem;
        width: 100%;
        height: 4.25rem;
        margin: 0 auto;
    }

    .brand {
        font-family: inherit;
        font-size: 1.6rem;
        font-weight: 600;
        line-height: 1.5;
        letter-spacing: -1px;
        color: var(--color-white-100);
        text-transform: uppercase;

        @media only screen and (max-width: 768px) {
            font-size: 1.3rem;
        }
    }

    .menu {
        position: fixed;
        top: -300px;
        left: 0;
        width: 100%;
        height: auto;
        padding: 4rem 0 3rem;
        overflow: hidden;
        background-color: var(--color-black-300);
        box-shadow: var(--shadow-medium);
        transition: all 0.4s ease-in-out;

        &.active {
            top: 0;
            width: 100%;
            height: auto;
        }

        &-inner {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            row-gap: 1.25rem;
        }

        &-link {
            font-family: inherit;
            font-size: 1rem;
            font-weight: 500;
            line-height: 1.5;
            color: var(--color-white-100);
            text-transform: uppercase;
            transition: all 0.3s ease;
        }

        &-block {
            display: inline-block;
            font-family: inherit;
            font-size: 0.875rem;
            font-weight: 500;
            line-height: 1.25;
            user-select: none;
            white-space: nowrap;
            text-align: center;
            margin-left: auto;
            padding: 0.65rem 1.5rem;
            border-radius: 3rem;
            text-transform: capitalize;
            box-shadow: var(--shadow-medium);
            transition: background-color 0.3s ease-in-out;
            background-color: var(--buttonColor);
            color: #fff;

                &:hover {
                    background-color: var(--buttonHoverColor, var(--buttonColor));
                }
        }

        // Media Query Breakpoint
        @media only screen and (min-width: 48rem) {
            position: relative;
            top: 0;
            width: auto;
            height: auto;
            padding: 0rem;
            margin-left: auto;
            background: none;
            box-shadow: none;

            &-inner {
                display: flex;
                flex-direction: row;
                column-gap: 2rem;
                margin: 0 auto;
            }

            &-link {
                text-transform: capitalize;
            }

            &-block {
                margin-left: 2rem;
            }
        }
    }

    .burger {
        position: relative;
        display: block;
        cursor: pointer;
        user-select: none;
        order: -1;
        z-index: 10;
        width: 1.6rem;
        height: 1.15rem;
        border: none;
        outline: none;
        background: none;
        visibility: visible;
        transform: rotate(0deg);
        transition: 0.35s ease;

        @media only screen and (min-width: 48rem) {
            display: none;
            visibility: hidden;
        }

        &-line {
            position: absolute;
            display: block;
            left: 0;
            width: 100%;
            height: 2px;
            border: none;
            outline: none;
            opacity: 1;
            border-radius: 1rem;
            transform: rotate(0deg);
            background-color: var(--color-white-100);
            transition: 0.25s ease-in-out;

            &:nth-child(1) {
                top: 0px;
            }
            &:nth-child(2) {
                top: 0.5rem;
                width: 70%;
            }
            &:nth-child(3) {
                top: 1rem;
            }
        }

        &.is-active .burger-line {
            &:nth-child(1) {
                top: 0.5rem;
                transform: rotate(135deg);
            }
            &:nth-child(2) {
                opacity: 0;
                visibility: hidden;
            }
            &:nth-child(3) {
                top: 0.5rem;
                transform: rotate(-135deg);
            }
        }
    }
</style>