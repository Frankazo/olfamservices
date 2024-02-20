<script></script>

<main class="main">
    <section class="section banner banner-section">
       <div class="container banner-column">
          <img class="banner-image" src="images/hero.jpg" alt="banner">
          <div class="banner-inner">
             <h1 class="heading-xl">Olfam Services <br> General Contractor</h1>
             <p class="paragraph">
               Transforming Dreams into Reality! <br> Request Your Quote Today and Build with Confidence!
             </p>
             <a href="#contact" class="btn btn-darken btn-inline">
                Request a Quote<i class="bx bx-right-arrow-alt"></i>
             </a>
          </div>
          <!-- <div class="banner-links">
             <a href="#" title=""><i class="bx bxl-facebook"></i></a>
             <a href="#" title=""><i class="bx bxl-instagram"></i></a>
             <a href="#" title=""><i class="bx bxl-twitter"></i></a>
             <a href="#" title=""><i class="bx bxl-youtube"></i></a>
          </div> -->
       </div>
    </section>
 </main>

<style lang="scss">
// Banner Section
.banner {
   color: #fff;
   padding: 5rem 0;

   h1 {
      font-size: clamp(2rem, 3vw, 4rem);
      // font-size: 2.2rem;
      text-wrap: nowrap;
   }
   &-column {
      position: relative;
      display: grid;
      align-items: center;
      row-gap: 3rem;
      padding: 0;

      // Media Query Breakpoint
      @media only screen and (min-width: 48rem) {
         width: 100%;
         display: flex;
         max-width: none;
         justify-content: flex-end;
         padding: 0;
         gap: 5%;
         // grid-template-columns: repeat(2, minmax(0, 1fr));
         // justify-content: center;
      }

      @media only screen and (min-width: 64rem) {
      //    // grid-template-columns: 1fr max-content;
      //    // column-gap: 4rem;
      //    // margin-top: 3rem;

      //    margin: 0;
      //    width: 100%;
      //    display: flex;
      //    max-width: none;
      //    justify-content: flex-end;
      //    padding: 0;
         gap: 10%;
      }
   }

   &-image {
      display: block;
      // max-width: 18rem;
      height: auto;
      margin-top: 2rem;
      object-fit: cover;
      justify-self: center;

      max-width: none;
      width: 100%;
      padding: 0;

      // Media Query Breakpoint
      @media only screen and (min-width: 48rem) {
         order: 1;
         // max-width: 20rem;
         width: auto;
         max-width: 50%;
         height: auto;
         margin: 0;
      }

      // @media only screen and (min-width: 64rem) {
      //    // max-width: 25rem;
      //    // max-width: 35rem;
      //    // height: auto;
      //    max-width: 50%;
      //    margin: 0;
      //    // margin-right: 5rem;
      // }
   }

   &-inner {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      row-gap: 1.75rem;
      padding: 0 20px;


      // @media only screen and (min-width: 48rem) {
      //    padding: 0;
      // }
   }

   // &-links {
   //    position: absolute;
   //    top: 30%;
   //    right: 1.5rem;
   //    display: grid;
   //    justify-items: center;
   //    row-gap: 0.5rem;
   //    opacity: 0;
   //    visibility: hidden;

   //    // Media Query Breakpoint
   //    @media only screen and (min-width: 64rem) {
   //       opacity: 1;
   //       visibility: visible;
   //    }

   //    & > * {
   //       font-size: 1.25rem;
   //       line-height: 1.25;
   //       color: var(--color-white-100);
   //    }

   //    &::before {
   //       position: absolute;
   //       content: "";
   //       top: -3rem;
   //       width: 4rem;
   //       height: 1.5px;
   //       transform: rotate(90deg);
   //       background: var(--color-white-100);
   //    }

   //    &::after {
   //       position: absolute;
   //       content: "";
   //       bottom: -3rem;
   //       width: 4rem;
   //       height: 2px;
   //       transform: rotate(90deg);
   //       background: var(--color-white-100);
   //    }
   // }
}

</style>