<!-- Header.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte'; 
  import ThemeSwitch from '$lib/components/molecules/ThemeSwitch.svelte';
  import Modal from '$lib/components/atoms/Modal.svelte';
  import Button from '$lib/components/atoms/FloatingButton.svelte';
  import Card from '$lib/components/atoms/Card.svelte';
  let showModal = false;
</script>

<header>
  <nav>
    <ul>
      <li>
        <a class="header-logo" href="/">david han</a>
      </li>
      <!-- <li> -->
      <!--   <span>|</span> -->
      <!-- </li> -->
      <li>
        <a href="/blog">blog</a>
      </li>
      <li>
        <a href="/about">about</a>
      </li>
      <li>
        <a href="/contact">contact</a>
      </li>
      <!-- <li> -->
      <!--   <Card /> -->
      <!--         </li>  -->
      <!-- <li> -->
      <!--   <ThemeSwitch width='1.4rem' height='2.1rem'/> -->
      <!-- </li> -->
    </ul>
    <Button on:click={() => (showModal = true)} size="small">
      <Icon name='settings'/>
    </Button>
  </nav>
</header>

<Modal bind:showModal>
	<h2 slot="header">
		settings	
	</h2>

  <div> 
    <ThemeSwitch /> toggle theme
  </div>
	<a href="https://www.merriam-webster.com/dictionary/modal">merriam-webster.com</a>
</Modal>

<!-- Component Styling -->
<style lang="scss">
  @import "../../styles/themes.scss";
  :global(body) header {
    //margin: 0;
    margin-top: 2rem;
    margin-bottom: 2rem;
    background: $light-theme-bg;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;   
    align-content: start;
    font-size: 1.6rem;
  }

  :global(body.dark) header {
    background: $dark-theme-bg;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    gap: 1rem;
    //align-items: center;
  }

  :global(body) .header-logo {
    font-weight: bold;
    text-align: center;
    padding: 0.1rem;
    background: $dark-theme-accent;
    box-shadow: 0.15rem 0.15rem $dark-theme-bg;
  }

  :global(body) .header-logo:hover {
    text-decoration: none;
    filter: brightness(95%);
  }

  :global(body.dark) .header-logo {
    background: $light-theme-accent;
    box-shadow: 0.15rem 0.15rem $light-theme-bg;
  }

  :global(body.dark) .header-logo:hover {
    text-decoration: none;
    filter: brightness(95%);
  }

  :global(body) a {
    text-decoration: none;
    color: $light-theme-text; 
  }

  a:hover {
    text-decoration: underline;
  }

  :global(body.dark) a {
    color: $dark-theme-text;
  }
</style>
