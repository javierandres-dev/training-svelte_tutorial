<script>
  const emojis = {
    car: '🚗',
    motorcycle: '🏍️',
    truck: '🚚',
    bus: '🚌',
  };

  export let name;

  const emoji = emojis[name];
</script>

<p>The emoji for {name} is {emoji}</p>
