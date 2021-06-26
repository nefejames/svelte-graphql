<script>
  import { getClient, query } from "svelte-apollo";
  import { gql } from "apollo-boost";
  const GET_TODOS = gql`
    {
      getTodos {
        id
        text
        done
      }
    }
  `;

  const client = getClient();

  const todos = query(client, { query: GET_TODOS });
</script>

<h1>Todos</h1>
