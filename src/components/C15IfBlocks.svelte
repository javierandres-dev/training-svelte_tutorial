<script>
  let loggedIn = false;

  const toggle = () => (loggedIn = !loggedIn);
</script>

{#if loggedIn}
  <button on:click={toggle}>Log out</button>
{/if}

{#if !loggedIn}
  <button on:click={toggle}>Log in</button>
{/if}
