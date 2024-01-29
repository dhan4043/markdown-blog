<script>
	export let filename;
	export let lang;
	export let fullBleed = undefined;
</script>

<div class="code-block" class:full-bleed={fullBleed}>
	{#if filename}
		<div class="filename">{filename}</div>
	{/if}
	{#if lang}
		<div class="lang">{lang}</div>
	{/if}
	<slot />
</div>

<style lang="scss">
  @import "../../styles/themes.scss";
	.code-block {
		display: block;
		position: relative;
		//background-color: var(--color--code-background);
    background-color: $dark-theme-bg;
		color: $dark-theme-text;
		font-family: 'Menlo';
		font-size: 1.25rem;
		border-radius: 0.5rem;
		box-shadow: var(--card-shadow);

		padding: 30px 15px;
		margin: 30px 0;

		:global(pre) {
			overflow-x: auto;
			scrollbar-color: var(--color--primary) var(--color--primary-tint);
			scrollbar-width: thin;
			padding-bottom: 5px;

			&::-webkit-scrollbar {
				height: 8px;
			}
			&::-webkit-scrollbar-thumb {
				background: var(--color--primary);
				&:hover {
					background: var(--color--primary-shade);
				}
			}
		}

		.lang {
			position: absolute;
			right: 0;
			top: -15px;
			background: inherit;
			border-radius: 8px;
			padding: 5px 10px;
			z-index: 2;
			font-size: 0.85em;
		}

		.filename {
			background: inherit;
			border-top-left-radius: 8px;
			border-top-right-radius: 8px;
			margin-bottom: -2px;
			padding: 5px 10px;
			position: absolute;
			left: 0px;
			top: -15px;
			z-index: 1;
		}
	}
</style>
