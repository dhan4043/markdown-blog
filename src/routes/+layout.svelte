<!-- +layout.svelte -->
<script>
  import Header from '$lib/components/organisms/Header.svelte';
  import Footer from '$lib/components/organisms/Footer.svelte';
  import { fade } from 'svelte/transition';
  import '$lib/styles/style.scss';
  import '$lib/styles/blog.scss';

  export let data;
</script>

<Header/>

{#key data.currentRoute}
	<main in:fade={{ duration: 100, delay: 100 }} out:fade={{ duration: 100 }}>
		<slot />
	</main>
{/key}

<Footer/>
