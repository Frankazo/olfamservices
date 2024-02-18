<script>
    export let scroll;
    let scrollTop = 0;
    let scrollState = '';

    const handleScroll = () => {
        if (scroll > 80) {
            scrollState = scroll > scrollTop ? 'scrolling' : 'up';
        } else {
            scrollState = '';
        }

        scrollTop = scroll;
    };
</script>
<svelte:window on:scroll={handleScroll}/>

<section class="navbarWrapper {scrollState}">
    <div class="container-fluid">
        <nav class="navbar navbar-expand-md navbar-dark">
            <a class="navbar-brand heading-black" href="index.html">
                Olfam Services
            </a>
            <button class="navbar-toggler navbar-toggler-right border-0" type="button" data-toggle="collapse"
                    data-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false"
                    aria-label="Toggle navigation">
                <span data-feather="grid"></span>
            </button>
            <!-- <div class="collapse navbar-collapse" id="navbarCollapse">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <a class="nav-link page-scroll" href="#features">Features</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link page-scroll" href="#pricing">Pricing</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link page-scroll" href="#faq">FAQ</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link page-scroll" href="#blog">Blog</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link page-scroll d-flex flex-row align-items-center text-primary" href="#">
                            Try Generator
                        </a>
                    </li>
                </ul>
            </div> -->
        </nav>
    </div>
</section>

<style lang="scss">
    .navbarWrapper {
        position: fixed;
        top: 0;
        z-index: 1020;
        width: 100%;
        transition: all .3s ease-out;

        &.scrolling {
            transform: translateY(-100%);
            
            &.up {
                background-color: rgba(0, 0, 0, 0.9);
                transform: translateY(0);
                transition: all .3s ease-out;
            }
        }
    }

    .navbar {
        position: relative;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-pack: justify;
        justify-content: space-between;
        padding: 1.5rem 1.25rem;
    }

    .navbar {
    
        &.navbar-transparent {
            opacity: 0.98;
        }

        @media (max-width: 992px) {
            &.navbar-transparent {
                background-color: #000;
            }
        }
        
        .navbar-brand {
            font-size: 1.5rem;
            font-weight: 900;
            color: #1de9b6;
            text-transform: uppercase;
        }

        .navbar-nav .nav-item {
            margin: 0 .7rem;

            .nav-link {
                font-weight: 600;
            }
        }

    }
    .navbar-toggler {
        padding: 0.25rem 0.75rem;
        font-size: 1.25rem;
        line-height: 1;
        background-color: transparent;
        border: 2px solid transparent;
        border-radius: 0.3rem;
    }

    .navbar-dark .navbar-toggler {
        color: rgba(255, 255, 255, 0.7);
        border-color: rgba(255, 255, 255, 0.1);
    }
    .container-fluid {
        width: 100%;
        padding-right: 15px;
        padding-left: 15px;
        margin-right: auto;
        margin-left: auto;
    }
    .navbar-brand {
        display: inline-block;
        padding-top: 0.0625rem;
        padding-bottom: 0.0625rem;
        margin-right: 1.25rem;
        font-size: 1.25rem;
        line-height: inherit;
        white-space: nowrap;
    }

    .navbar-collapse {
        -ms-flex-preferred-size: 100%;
        flex-basis: 100%;
        -ms-flex-positive: 1;
        flex-grow: 1;
        -ms-flex-align: center;
        align-items: center;
    }

    .navbar-nav {
        display: -ms-flexbox;
        display: flex;
        justify-content: flex-end;
        -ms-flex-direction: column;
        flex-direction: column;
        padding-left: 0;
        margin-bottom: 0;
        list-style: none;
    }

    .ml-auto, .mx-auto {
        margin-left: auto !important;
    }

    .navbar.s .navbar-nav .nav-item {
        margin: 0 0.7rem;
    }

    .navbar.s .navbar-nav .nav-item .nav-link.s {
        font-weight: 600;
    }

    .navbar .navbar-nav .nav-item .nav-link {
        font-weight: 600;
    }

    .navbar-dark .navbar-nav .nav-link {
        color: #000;
    }

    .navbar-nav .nav-link {
        padding-right: 0;
        padding-left: 0;
    }

    .nav-link {
        display: block;
        padding: 0.25rem 1rem;
    }

    @media (min-width: 768px) {
        .navbar-expand-md {
            -ms-flex-flow: row nowrap;
            flex-flow: row nowrap;
            -ms-flex-pack: start;
            justify-content: flex-start;
        }  

        .navbar-expand-md .navbar-nav {
            -ms-flex-direction: row;
            flex-direction: row;
        }

        .navbar-expand-md .navbar-nav .nav-link {
            padding-right: 0.75rem;
            padding-left: 0.75rem;
        }
    }
</style>