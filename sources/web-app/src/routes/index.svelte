<script>
  import Sidebar from '../components/Sidebar.svelte';
  import Items from '../components/Items.svelte';
</script>

<style>
  article {
    display: grid;
    grid-template-columns: 1fr 11fr;
    grid-template-rows: 1fr;
    grid-gap: min(0.25vw, 0.25vh);
    grid-template-areas:
      'sidebar contents'
    ;

    height: 100%;
  }

  aside {
    grid-area: sidebar;

    background-color:aquamarine;
  }

  section {
    grid-area: contents;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: min(0.25vw, 0.25vh);
  }
</style>

<svelte:head>
  <title>Macarons Shop Berlin</title>
</svelte:head>

<article>
  <aside>
    <Sidebar />
  </aside>
  <section>
    <Items />
  </section>
</article>