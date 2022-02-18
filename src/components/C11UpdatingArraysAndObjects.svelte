<script>
  let numbers = [1, 2, 3, 4];

  const addNumber = () => (numbers = [...numbers, numbers.length + 1]);

  $: sum = numbers.reduce((a, b) => a + b);
</script>

<p>numbers: {numbers.join(' + ')}</p>
<p>sum: {sum}</p>
<button on:click={addNumber}>Add number</button>
