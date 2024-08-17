<script lang="ts">
  import Button from "$lib/Button.svelte";
  import TextInput from "$lib/TextInput.svelte";
  import DropDown from "$lib/DropDown.svelte";
  import DropDownItem from "$lib/DropDownItem.svelte";
</script>

<Button text="Pieslēgties" />
<br />
<TextInput />
<br />
<DropDown dropdown_text={"Darbība"}>
  <DropDownItem onclick={() => console.log("aa")}>aa</DropDownItem>
</DropDown>
<br />
