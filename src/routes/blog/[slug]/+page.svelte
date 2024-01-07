<!-- src/routes/[slug]/+page.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte';
  export let data;
  const {title, date, tags, Content} = data;
</script>

<article>
  <h1>{title}</h1>
  <p>Published: {date}</p>
  <Content />
  {#if data.tags.length}
	  <aside>
		  <h2>Posted in:</h2>
		  <ul>
			  {#each data.tags as tag}
				  <li>
					  <a href="/blog/tags/{tag}">
						  {tag}
					  </a>
				  </li>
			  {/each}
		  </ul>
	  </aside>
  {/if}
</article>

<!-- Article Layout -->
<style>
  article {
    padding: auto;
    overflow-wrap: break-word;
  }
</style>
