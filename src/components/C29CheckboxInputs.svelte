<script>
  let yes = false;
</script>

<label>
  <input type="checkbox" bind:checked={yes} />
  Do you want enable the button?
</label>

{#if yes}
  <p>Yes!</p>
{:else}
  <p>No</p>
{/if}

<button disabled={!yes}>{yes ? 'Enable' : 'Disable'}</button>
