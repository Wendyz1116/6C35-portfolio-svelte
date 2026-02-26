<script>
  export let data = {};
</script>

<article>
  <img src={data.image} alt="" />
  <div>
    <h2>{data.title}</h2>
    <p>{data.author}</p>
  </div>
</article>

<style>
  article {
    display: grid;
    grid-template-rows: subgrid;
    grid-row: span 2;
  }

  img {
    width: 30%;
    height: auto;
  }

  h2 {
    margin: 0;
  }
</style>
