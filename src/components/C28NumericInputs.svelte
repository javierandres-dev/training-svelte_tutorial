<script>
  let a = 1,
    b = 2;
</script>

<label>
  <input type="number" bind:value={a} />
  <input type="range" bind:value={a} />
</label>

<label>
  <input type="number" bind:value={b} />
  <input type="range" bind:value={b} />
</label>

<p>{a} + {b} = {a + b}</p>
