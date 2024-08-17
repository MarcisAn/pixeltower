<script lang="ts">
  let expanded = false;
  export let dropdown_text :string; 
</script>

<div id="container">
  <div class="dropdown">
    <button
      on:click={() => {
        expanded = !expanded;
      }}
      class="dropbtn"><img src="/triangle.png" alt="" />{dropdown_text}</button
    >
    {#if expanded}
    <div class="dropdown-content" on:click={() => expanded = false}>
        <slot><!-- optional fallback --></slot>
    </div>
    {/if}
  </div>
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
  .dropdown-content{
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
