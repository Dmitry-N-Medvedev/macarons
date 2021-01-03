<script>
  export let id;
  export let title;
  export let graphics;
</script>

<style>
  div {
    display: grid;
    height: 50vh;

    background-color: aquamarine;
  }

  img {
    background-color: brown;
    width: 100%;
    height: auto;
    object-fit: contain;
  }
</style>

<div {id}>
  <img src={graphics.image} {title} alt={title} />
</div>
