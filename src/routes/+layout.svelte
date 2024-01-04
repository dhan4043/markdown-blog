<!-- +layout.svelte -->
<script>
  import Header from '$lib/components/organisms/Header.svelte';
  import Footer from '$lib/components/organisms/Footer.svelte';
  import '$lib/styles/style.scss';
  import '$lib/styles/blog.scss';
</script>

<Header/>

<main>
	<slot />
</main>

<Footer/>
