<script>
  let count = 0;

  const increment = () => count++;
</script>

<button on:click={increment}>
  CLicked {count}
  {count === 1 ? 'time' : 'times'}
</button>
