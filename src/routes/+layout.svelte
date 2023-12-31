<!-- +layout.svelte -->
<script>
  import Header from '$lib/components/organisms/Header.svelte';
  import Footer from '$lib/components/organisms/Footer.svelte';
</script>

<Header/>

<main>
	<slot />
</main>

<Footer/>
