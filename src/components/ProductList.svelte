<script>
  import { getContext } from "svelte";
  const productCount = getContext("productCount-context");
  import BuyButton from "./BuyButton.svelte";
</script>

<div class="container">
  <ul>
    <!-- {#each products as product}
      <li>{product}</li>
    {/each} -->
    {#each Array(productCount) as product, i}
      <li>Producto {i + 1}</li>
    {/each}
  </ul>
  <BuyButton />
</div>

<style>
  ul {
    list-style-type: none; /* Elimina los puntos */
    padding-left: 0; /* Elimina la sangría predeterminada */
    text-align: center; /* Centra el texto de los elementos de la lista */
    border: 1px solid black;
    padding: 20px 20px;
    border-radius: 10px;
    background-color: rgb(207, 206, 206);
  }

  .container {
    width: 80%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center; /* Alinea los elementos hijos en el centro */
  }
</style>
