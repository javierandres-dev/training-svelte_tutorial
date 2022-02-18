<script>
  const x = 10;
</script>

{#if x > 10}
  <p>{x} is greater than 10</p>
{:else if x < 10}
  <p>{x} is less than 10</p>
{:else}
  <p>{x} is equal than 10</p>
{/if}
