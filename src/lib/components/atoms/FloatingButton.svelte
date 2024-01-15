<!-- FloatingButton.svelte -->
<script>
  import { HttpRegex } from "$lib/utils"

  export let color = ""
  export let style = ""
  export let size = ""
  export let href = undefined

  export let additionalClass = undefined

  const isExternalLink = !!href && HttpRegex.test(href)
  export let target = isExternalLink ? "_blank" : "_self"
  export let rel = isExternalLink ? "noopener noreferrer" : undefined

  $: tag = href ? "a" : "button"
  $: linkProps = {
    href,
    target,
    rel
  }
</script>

<svelte:element
	this={tag}
	{...linkProps}
	class={['button', `style--${style}`, `size--${size}`, `color--${color}`, additionalClass].join(
		' '
	)}
	data-sveltekit-preload-data
	on:click
	{...$$restProps}
>
	{#if $$slots['icon']}
		<div class="icon">
			<slot name="icon" />
		</div>
	{/if}
	<slot />
</svelte:element>

<style>
  :global(body) button {
	  position:fixed;
  	width:3rem;
	  height:3rem;
	  bottom:2rem;
	  right:2rem;
    background-color: transparent;
	  //border-color:#282828;
    //border-style: solid;
    border-style: none;
	  color:#282828;
	  border-radius:50%;
	  text-align:center;
	  margin-top:2rem;
  }

  :global(body.dark) button {
    //border-color:#fffff5;
    color:#fffff5;
  }
</style>
