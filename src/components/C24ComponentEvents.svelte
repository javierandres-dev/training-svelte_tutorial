<script>
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();

  const sayHello = () => {
    dispatch('myEvent', {
      text: 'Hello',
    });
  };
</script>

<button on:click={sayHello}>Click to say hello</button>
