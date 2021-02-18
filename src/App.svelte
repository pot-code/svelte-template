<script>
  import Sidebar from './components/Sidebar/Sidebar.svelte';

  import { routes } from './routes.js';

  function changeRoute(idx) {
    console.log('selected route', routes[idx]);
  }
</script>

<main>
  <section class="sidebar">
    <Sidebar {routes} onChange={changeRoute} />
  </section>
</main>

<style>
  main {
    display: flex;
    flex-direction: row;
  }
  section.sidebar {
    width: 13%;
    flex-grow: 0;
    flex-shrink: 0;
    height: 100vh;
    background-color: #000c1c;
  }

  @media screen and (min-width: 1440px) {
    section.sidebar {
      width: 13%;
    }
  }

  @media screen and (min-width: 1024px) {
    section.sidebar {
      width: 15%;
    }
  }

  @media screen and (max-width: 768px) {
    section.sidebar {
      display: none;
    }
  }
</style>
