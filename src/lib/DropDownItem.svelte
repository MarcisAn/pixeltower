<script lang="ts">
export let onclick;
</script>


<button class="dropdown-item" on:click={onclick}>
  <slot><b>Dropdown item not provided.</b></slot>
</button>

<style>
  @font-face {
    font-family: "pixelify";
    src: url("/pixelifysans.ttf");
  }

  button {
    font-family: "pixelify";
    border-width: 10px;
    border-style: solid;
    border-image: url(/border.png) 25% round;
    background-color: #ffe694;
    font-size: x-large;
    cursor: pointer;
  }
  .dropdown-content {
    display: flex;
    flex-direction: column;
    width: fit-content;
  }
  .dropdown-item {
    background-color: #fff2c8;
    padding: 7px;
    font-family: "pixelify";
    border-image: url(/border.png) 25% round;
    border-width: 10px;
    border-style: solid;
  }
  img {
    margin-right: 10px;
  }
  button:active {
    box-shadow: 5px 5px 5px rgb(194, 158, 92);
  }
  button:hover {
    background-color: #ffefbb;
  }
</style>
