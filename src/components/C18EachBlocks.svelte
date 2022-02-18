<script>
  const colors = ['green', 'blue', 'red'];

  const users = [
    { name: 'pepita', nin: 123 },
    { name: 'pepito', nin: 456 },
  ];
</script>

<ul>
  {#each colors as color, i}
    <li>{i + 1}. Color: <span style="color: {color};">{color}</span></li>
  {/each}
</ul>

<ul>
  {#each users as { name, nin }}
    <li>Name: {name}, Nin: {nin}</li>
  {/each}
</ul>
