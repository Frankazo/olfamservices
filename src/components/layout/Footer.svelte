

<footer class="footer-section">
    <div class="container">
        <div class="footer-cta pt-5 pb-5">
            <div class="row">
                <div class="col-xl-4 col-md-4 mb-30">
                    <div class="single-cta">
                        <div class="cta-text">
                            <h4>Find us</h4>
                            <span>Address Coming Soon</span>
                        </div>
                    </div>
                </div>
                <div class="col-xl-4 col-md-4 mb-30">
                    <div class="single-cta">
                        <div class="cta-text">
                            <h4>Call us</h4>
                            <span>Number Coming Soon</span>
                        </div>
                    </div>
                </div>
                <div class="col-xl-4 col-md-4 mb-30">
                    <div class="single-cta">
                        <div class="cta-text">
                            <h4>Mail us</h4>
                            <a href="mailto:olfamservices@gmail.com" target="_blank">olfamservices@gmail.com</a>  
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="copyright-area">
        <div class="container">
            <div class="row">
                <div class="col-xl-6 col-lg-6 text-center text-lg-left">
                    <div class="copyright-text">
                        <p>Copyright &copy; 2024 Olfam Services, All Right Reserved</p>
                    </div>
                </div>
                <div class="col-xl-6 col-lg-6 d-none d-lg-block text-right">
                    <div class="footer-menu">
                        <ul>
                            <li><a href="#top">Home</a></li>
                            <li><a href="#about">About</a></li>
                            <li><a href="#services">Services</a></li>
                            <!-- <li><a href="#projects">Projects</a></li> -->
                            <li><a href="#contact">Contact</a></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</footer>

<style lang="scss">
    ul {
        margin: 0px;
        padding: 0px;
    }
    .row {
        display: flex;
        justify-content: space-around;
        
    }
    .footer-section {
        background: #151414;
        position: relative;
    }
    .footer-cta {
        padding: 15px;
    }
    
    .cta-text {
        padding-left: 15px;
        display: inline-block;
    }
    .cta-text h4 {
        color: #fff;
        font-size: 20px;
        font-weight: 600;
        margin-bottom: 2px;
    }
    .cta-text span {
        color: #757575;
        font-size: 15px;
    }
    
    .footer-widget ul li {
        display: inline-block;
        float: left;
        width: 50%;
        margin-bottom: 12px;
    }

    .footer-widget ul li a:hover{
        color: #ff5e14;
    }

    .footer-widget ul li a {
        color: #878787;
        text-transform: capitalize;
    }
    
    .copyright-area{
        background: #202020;
        padding: 25px 0;
    }

    .copyright-text p {
        margin: 0;
        font-size: 14px;
        color: #878787;
    }
    
    .footer-menu li {
        display: inline-block;
        margin-left: 20px;
    }

    .footer-menu li:hover a{
        color: #ff5e14;
    }

    .footer-menu li a {
        font-size: 14px;
        color: #878787;
    }

    @media only screen and (max-width: 768px) {
        .row {
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
    }

</style>