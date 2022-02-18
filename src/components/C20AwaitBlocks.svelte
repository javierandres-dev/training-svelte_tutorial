<script>
  let promise;

  const makeApromise = () => {
    promise = new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve(' Success!');
      }, 1000);
    });

    promise.then((successMessage) =>
      console.log('if resolve:' + successMessage)
    );
  };
</script>

{#await promise then value}
  <p>Short block - Value: {value}</p>
{/await}

{#await promise}
  <p>Then block - Promise is pending</p>
{:then value}
  <p>Then block - Value: {value}</p>
{/await}

{#await promise}
  <p>Catch block - Promise is pending</p>
{:then value}
  <p>Catch block - Value: {value}</p>
{:catch error}
  <p>Cath block - Error: {error}</p>
{/await}

<button on:click={makeApromise}>Make a promise</button>
