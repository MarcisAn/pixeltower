<script lang="ts">
  export let text: string;
</script>

<div id="container">
  <button>{text}</button>
</div>

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
  button:active {
    box-shadow: 5px 5px 5px rgb(194, 158, 92)
  }
  button:hover {
    background-color: #ffefbb;
  }
</style>
