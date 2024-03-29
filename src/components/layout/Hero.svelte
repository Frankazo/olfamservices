<script>
   import LogoFinal from "../../assets/LogoFinal.svelte";
</script>

<div class="hero" style="background-image: url(images/hero.jpg)">
  <div class="hero-text">
      <div class="logo"><LogoFinal /></div>
      <h1>Transforming Dreams into Reality!</h1>
      <p>Request Your Quote Today and Build with Confidence!</p>
      <div class="cta">
         <a href="#services" class="button">Our Services</a>
         <a href="#contact" class="button button--white ">Request a Quote</a>
      </div>
  </div>
  <div class="overlay"></div>
</div>

<style lang="scss">
   .hero {
      min-height: 100vh;
      height: 100%;
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
      position: relative;

      .hero-text {
         position: absolute;
         width: 100%;
         height: 100%;
         display: flex;
         flex-direction: column;
         justify-content: center;
         align-items: center;
         text-align: center;
         color: white;
         margin: auto;
         z-index: 10;

         .logo {
            width: 250px;
            height: 280px;
         }

         h1 {
            font-weight: bold;
            font-style: italic;
            font-size: clamp(2rem, 3vw, 3rem);
         }

         p {
            font-size: clamp(0.8rem, 3vw, 1.3rem);
         }

         .cta {
            display: flex;
            gap: 20px;
            margin-top: 50px;
         }
      }

      @media screen and (max-width: 767px) {

         .hero-text {
            .logo {
               width: 150px;
            }


            .cta {
               flex-direction: column;
            }
         }
      }
   }
</style>