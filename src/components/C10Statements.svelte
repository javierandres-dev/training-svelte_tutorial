<script>
  let count = 0;

  const increment = () => count++;

  $: double = count * 2;
  $: {
    if (count > 5) {
      alert('maximum allowed: 5');
      count = 5;
    }
  }
</script>

<p>count: {count}</p>
<p>double: {double}</p>
<button on:click={increment}>Click me</button>
