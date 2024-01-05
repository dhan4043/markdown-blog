<!-- src/routes/[slug]/+page.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte';
  export let data;
  const {title, date, Content} = data;
</script>

<article>
  <h1>{title}</h1>
  <p>Published: {date}</p>
  <Content />
</article>
