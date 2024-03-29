<div class="container">
    <div class="row justify-content-center text-center">
        <div class="col-md-10 col-lg-8">
            <div class="header-section">
                <h2 class="title">Exclusive <span>Services</span></h2>
                <p class="description">Each of our services is backed by a commitment to excellence, combining skilled craftsmanship with premium materials to bring your vision to life. Partner with us for a construction experience that exceeds expectations, delivering lasting value to your property.</p>
            </div>
        </div>
    </div>
</div>

<style lang="scss">
    .container {
        padding-top: 110px;
        padding-bottom: 120px;
        font-family: "Poppins", sans-serif;
        color: #000;
    }

    .header-section {
        margin-bottom: 35px;
    }

    .header-section .title {
        position: relative;
        margin-bottom: 40px;
        padding-bottom: 25px;
        text-transform: uppercase;
        font-weight: 700;
    }

    .header-section .title:before {
        content: "";
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        width: 140px;
        height: 1px;
        background-color: var(--accent);
    }

    .header-section .title:after {
        content: "";
        position: absolute;
        bottom: -1px;
        left: 50%;
        transform: translateX(-50%);
        width: 45px;
        height: 3px;
        background-color: var(--accent);
    }

    .header-section .title span {
        color: var(--accent);
    }

    .header-section .description {
        color: #6f6f71;
    }
</style>