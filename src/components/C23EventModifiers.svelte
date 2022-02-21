<script>
  const handleClick = () => {
    alert('event modifier example');
  };
</script>

<button on:click|once={handleClick}>Click me</button>
