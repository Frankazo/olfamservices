<script>
  // layout
  import Navigation from "./components/layout/Navigation.svelte";
	import Footer from './components/layout/Footer.svelte';

  // pages
  import Home from "./components/pages/Home.svelte";
  import About from "./components/pages/About.svelte";
  import Services from "./components/pages/Services.svelte";
  import Projects from "./components/pages/Projects.svelte";
  import Service from "./components/pages/Service.svelte";
  import Contact from "./components/pages/Contact.svelte"

  // helpers
  import ScrollTop from "./components/ScrollTop.svelte";
  let scroll;

  // Routing
  const routingMap = {
    '#home': Home,
    '#about': About,
    '#services': Services,
    '#projects': Projects,
    '#service': Service,
    '#contact': Contact,
  };

  if (!routingMap[location.hash]) window.location.href = '#home';
  let page = routingMap[location.hash] || Home;

  function routeChange() {
    if (!routingMap[location.hash]) window.location.href = '#home';
    page = routingMap[location.hash] || Home;
    document.body.scrollIntoView();
  };
</script>
<svelte:window on:hashchange={routeChange} bind:scrollY={scroll} />

<main>
  <Navigation {scroll}/>

  <svelte:component this={page} />

  <Footer />
  <ScrollTop {scroll}/>
</main>

<style>
  main {
    background-color: #fff;
  }
</style>
