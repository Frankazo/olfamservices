<script>
  // layout
  import Navigation from "./components/layout/Navigation.svelte";
	import Hero from './components/layout/Hero.svelte';
  import CopyBlock from "./components/shared/CopyBlock.svelte";
  import Featured from "./components/layout/Featured.svelte";
	import Services from './components/layout/Services.svelte';
  import ImageCarousel from "./components/layout/ImageCarousel.svelte";
	import ContactUs from './components/layout/ContactUs.svelte';
	import Footer from './components/layout/Footer.svelte';

  // helpers
  import ScrollTop from "./components/ScrollTop.svelte";
  let scroll;
</script>
<svelte:window bind:scrollY={scroll} />
<main>
  <Navigation {scroll}/>
  <Hero />
  <CopyBlock />
  <Featured />
  <Services />
  <ImageCarousel />
  <ContactUs />
  <Footer />
  <ScrollTop {scroll}/>
</main>

<style>
  main {
    background-color: #000;
  }
</style>
