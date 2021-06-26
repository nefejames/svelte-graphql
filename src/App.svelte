<script>
  import Todos from "./Todos.svelte";
  import ApolloClient from "apollo-boost";
  import { setClient } from "svelte-apollo";
  const client = new ApolloClient({
    uri: "http://todos-graphql.herokuapp.com/",
  });

  setClient(client);
</script>

<main>
  <h1>Svelte GraphQl Todo App</h1>
  <Todos />
</main>

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
    font-size: 2em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
