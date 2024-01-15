<!-- ThemeSwitch.svelte -->
<script>
  export let width = "1rem";
  export let height = "1rem";
  function toggle() {
    window.document.body.classList.toggle('dark')
  }
</script>

<button on:click={toggle}
  style="width: {width}; height: {height};"
>

	<slot/>
</button>

<style>
	button {
    width: 1rem;
    height: 1rem;
		background-color: #FA6800;
		color: #fffff5;
		border: none;
		border-radius: 4px;
		padding: 0;
	}

	:global(body.dark) button {
		background-color: #008A00;
		color: #fffff5;
	}
</style>
