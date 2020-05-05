<script>
  export let name;

  // fetch polyfill
  import "whatwg-fetch";

  // async arrow function test
  const exampleFetch = async () => {
    const response = await window.fetch(
      `https://jsonplaceholder.typicode.com/users/9`
    );
    const data = await response.json();
    return data;
  };

  let promise = exampleFetch();
</script>

<style>
  :root {
    --color: #ff3e00;
  }
  
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: var(--color);
    text-transform: uppercase;
    font-size: 3em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hoi, {name}!</h1>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>

  {#await promise}
    <pre>... it's fetching (I promise)</pre>
  {:then user}
    <p>rest api fetch result:</p>
    <pre>{user.name}</pre>
  {/await}

</main>
