<script>
  import { getContext } from "svelte";
  const productCount = getContext("productCount-context");
</script>

<button class="buy-button">
  <p>
    Buy <span>({productCount})</span>{productCount === 1
      ? " product "
      : " products "}
  </p>
</button>

<style>
  .buy-button {
    display: flex;
    align-items: center;
    background-color: #6b5c4d;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border-radius: 5px;
  }
</style>
