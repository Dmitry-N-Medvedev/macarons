<script>
  import {
    onMount,
  } from 'svelte';
  import Item from './Item.svelte';

  let items = [];

  const fetchItemDescriptions = async () => (await fetch('/items/items.json', {
    method: 'GET',
    mode: 'cors',
    cache: 'no-cache',
    credentials: 'same-origin',
    headers: {
      'Content-Type': 'application/json',
    },
    redirect: 'follow',
    referrerPolicy: 'no-referrer',
  })).json();

  onMount(async () => {
    items = await fetchItemDescriptions();
  });
</script>

{#each items as item}
  <Item
    id={item.id}
    title={item.title}
    graphics={item.graphics}
  />
{/each}
