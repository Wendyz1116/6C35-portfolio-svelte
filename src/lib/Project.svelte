<script>
  export let data = {};
</script>

<article>
  <h2>{data.title}</h2>
  <img src={data.image} alt="" />
  <p>
    {@html data.description}
  </p>
</article>

<style>
  article {
    display: grid;
    grid-template-rows: subgrid;
    grid-row: span 3;
  }

  h2 {
    margin: 0;
  }

  img {
    width: 100%;
    height: auto;
  }
</style>
