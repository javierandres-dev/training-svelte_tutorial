<script>
  let count = 0;

  $: double = count * 2;

  const increment = () => count++;
</script>

<p>count: {count}</p>
<p>double: {double}</p>
<button on:click={increment}>Click me</button>
