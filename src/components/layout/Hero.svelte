<script>

</script>

<div class="hero">
  <div class="hero-text">
    <h1>Transforming Dreams into Reality!</h1>
    <p>Request Your Quote Today and Build with Confidence!</p>
    <a href="#contact">Request a Quote</a>
  </div>
  <div class="overlay"></div>
</div>

<style lang="scss">
   .hero {
      min-height: 60vh;
      background-image: url("images/hero.jpg");
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

         h1 {
            font-weight: bold;
            font-style: italic;
            font-size: clamp(2rem, 3vw, 3rem);
         }

         p {
            font-size: clamp(0.8rem, 3vw, 1.3rem);
         }
      }

      .hero-text a {
         display: inline-block;
         font-family: inherit;
         font-size: 1rem;
         font-weight: 500;
         line-height: 1.25;
         user-select: none;
         white-space: nowrap;
         text-align: center;
         padding: 15px 60px;
         border-radius: 3rem;
         text-transform: capitalize;
         box-shadow: var(--shadow-medium);
         transition: background-color 0.3s ease-in-out;
         background-color: #00000088;
         color: #fff;
         margin-top: 50px;

            &:hover {
               background-color: #000;
            }
      }
      .overlay {
         position: absolute;
         top: 0;
         bottom: 0;
         left: 0;
         right: 0;
         background: rgba(0, 0, 0, 0.3);
      }
   }
</style>