<script>
  import { setContext } from "svelte";
  import ProductList from "./components/ProductList.svelte";
  import Carrito from "./lib/Carrito.svelte";

  let productCount = 6;

  setContext("productCount-context", productCount);
</script>

<main>
  <p><Carrito /> <span> {productCount} </span></p>

  <div>
    <h1>Carrito con Context</h1>
    <ProductList />
  </div>
</main>

<style>
  span {
    color: red;
    font-weight: 700;
  }
  main {
    border: 2px solid black;
    padding: 20px;
    border-radius: 10px;
    background-color: darkgrey;
  }
  p {
    display: inline-block;
    border: 1px solid black;
    padding: 20px 20px;
    border-radius: 10px;
    background-color: rgb(207, 206, 206);
  }
  div {
    border: 1px solid black;
    padding: 20px 20px;
    border-radius: 10px;
    background-color: rgb(207, 206, 206);
  }
</style>
