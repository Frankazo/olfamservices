<script>
  // layout
  import Navigation from "./components/layout/Navigation.svelte";
	import Hero from './components/layout/Hero.svelte';
	import Services from './components/layout/Services.svelte';
	import ContactUs from './components/layout/ContactUs.svelte';
	import Footer from './components/layout/Footer.svelte';

  import ScrollTop from "./components/ScrollTop.svelte";
  let scroll;
</script>
<svelte:window bind:scrollY={scroll} />
<main>
  <Navigation {scroll}/>
  <Hero />
  <Services />
  <ContactUs />
  <Footer />
  <ScrollTop {scroll}/>
</main>

<style>
  main {
    /* background-color: #ffffff; */
    color: #000;
  }
</style>
