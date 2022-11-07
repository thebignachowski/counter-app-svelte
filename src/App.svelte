<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number => (counter += value);
  const reset = () => (counter = 0);
</script>

<main>
  <h1>counter app</h1>
  <h2 class={counter < 0 ? "negative" : "positive"}>Counter: {counter}</h2>
  <button class="add" on:click={() => modifyCounter(1)}>+1</button>
  <button class="subs" on:click={() => modifyCounter(-1)}>-1</button>
  <button class="reset" on:click={reset}>reset</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1rem;
    max-width: 24rem;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 900;
    padding-bottom: 3rem;
    border-bottom: 1px solid #000;
  }
  h2 {
    font-size: 3.4rem;
  }
  .positive {
    color: olivedrab;
  }
  .negative {
    color: crimson;
  }
  button {
    padding: 1rem 2rem;
    font-size: 2.4rem;
    margin: 0 1rem;
    border-radius: 0.5rem;
    text-transform: uppercase;
  }
  button:last-of-type {
    margin: 0;
  }
  button:hover {
    cursor: pointer;
  }

  .add {
    background-color: #26d231;
  }
  .add:active {
    background-color: #19b623;
  }
  .subs {
    background-color: #3a9aea;
  }
  .subs:active {
    background-color: #2688d8;
  }
  .reset {
    background-color: tomato;
    color: #fff;
  }
  .reset:active {
    background-color: #b64531;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
