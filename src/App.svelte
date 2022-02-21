<script>
  import C20AwaitBlocks from './components/C20AwaitBlocks.svelte';
  import C15IfBlocks from './components/C15IfBlocks.svelte';
  import C01IntroductionBasics from './components/C01Basics.svelte';
  import C02IntroductionAddingData from './components/C02AddingData.svelte';
  import C03DynamicAttributes from './components/C03DynamicAttributes.svelte';
  import C04Styling from './components/C04Styling.svelte';
  import C05Nested from './components/C05Nested.svelte';
  import C06HtmlTags from './components/C06HtmlTags.svelte';
  import C07MakingAnApp from './components/C07MakingAnApp.svelte';
  import C08Assignments from './components/C08Assignments.svelte';
  import C09Declarations from './components/C09Declarations.svelte';
  import C10Statements from './components/C10Statements.svelte';
  import C11UpdatingArraysAndObjects from './components/C11UpdatingArraysAndObjects.svelte';
  import C12DeclaringProps from './components/C12DeclaringProps.svelte';
  import C13DefaultValues from './components/C13DefaultValues.svelte';
  import C14SpreadProps from './components/C14SpreadProps.svelte';
  import C16ElseBlocks from './components/C16ElseBlocks.svelte';
  import C17ElseIfBlocks from './components/C17ElseIfBlocks.svelte';
  import C18EachBlocks from './components/C18EachBlocks.svelte';
  import C19KeyedEachBlocks from './components/C19KeyedEachBlocks.svelte';
  import C21DomEvents from './components/C21DomEvents.svelte';
  import C22InlineHandlers from './components/C22InlineHandlers.svelte';
  import C23EventModifiers from './components/C23EventModifiers.svelte';
  import C24ComponentEvents from './components/C24ComponentEvents.svelte';

  export let name;

  const obj = {
    name: 'Pepita',
    country: 'Colombia',
  };

  let names = [
    { id: 'qwe', name: 'car' },
    { id: 'asd', name: 'motorcycle' },
    { id: 'zxc', name: 'truck' },
    { id: 'rty', name: 'bus' },
  ];

  const removeFirstItem = () => {
    names = names.slice(1);
  };
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</main>
<hr />
<aside>
  <h2>Events</h2>
  <C24ComponentEvents />
  <C23EventModifiers />
  <C22InlineHandlers />
  <br />
  <C21DomEvents />
  <h2>Logic</h2>
  <C20AwaitBlocks />
  <br />
  <button on:click={removeFirstItem}>Remove first item</button>
  {#each names as item (item.id)}
    <C19KeyedEachBlocks name={item.name} />
  {/each}
  {#each names as item}
    <C19KeyedEachBlocks name={item.name} />
  {/each}
  <C18EachBlocks />
  <C17ElseIfBlocks />
  <C16ElseBlocks />
  <br />
  <C15IfBlocks />
  <h2>Props</h2>
  <C14SpreadProps {...obj} />
  <C13DefaultValues aProp={'with custom value'} />
  <C13DefaultValues />
  <C12DeclaringProps aProp={'Works!'} />
  <C12DeclaringProps />
  <h2>Reactivity</h2>
  <C11UpdatingArraysAndObjects />
  <C10Statements />
  <C09Declarations />
  <br />
  <C08Assignments />
  <h2>Introduction</h2>
  <C07MakingAnApp />
  <C06HtmlTags />
  <C05Nested />
  <C04Styling />
  <C03DynamicAttributes />
  <C02IntroductionAddingData />
  <C01IntroductionBasics />
</aside>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
