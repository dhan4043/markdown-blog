<!-- Header.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte'; 
  import ThemeSwitch from '$lib/components/molecules/ThemeSwitch.svelte';
  import Modal from '$lib/components/atoms/Modal.svelte';
  import Button from '$lib/components/atoms/FloatingButton.svelte';
  import Card from '$lib/components/atoms/Card.svelte';
  let showModal = false;
  let themeIcon = "sun";
  function toggle() {
    (themeIcon === "sun") ? (themeIcon = "moon"): (themeIcon = "sun");
    window.document.body.classList.toggle('dark');
  }
</script>

<header>
  <a class="metro-logo" href="/">DH</a>

  <nav>
    <ul>
      <li>
        <a href="/blog">BLOG</a>
      </li>
      <li>
        <a href="/about">ABOUT</a>
      </li>
      <li>
        <a href="/contact">CONTACT</a>
      </li>
      <!-- <li> -->
      <!--   <Card /> -->
      <!--         </li>  -->
      <!-- <li> -->
      <!--   <ThemeSwitch width='1.4rem' height='2.1rem'/> -->
      <!-- </li> -->
    </ul>
    <Button on:click={toggle} size="small">
      <Icon name={themeIcon}/>
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
    line-height: 3.4rem;
    font-size: 1.7rem;
    font-family: 'Inter';
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
  }

  :global(body) .metro-logo {
    font-weight: bold;
    text-align: center;
    //padding: 0.2rem;
    background: #00B140;
    border-radius: 50%;
    height: 3.2rem;
    width: 3.2rem;
    color: $light-theme-bg;
  }

  :global(body) .metro-logo:hover {
    text-decoration: none;
    filter: brightness(95%);
  }

  :global(body.dark) .metro-logo {
    background: $dark-theme-accent;
    color: $dark-theme-bg;
  }

  :global(body) .header-logo {
    font-weight: bold;
    text-align: center;
    padding: 0.1rem;
    background: $dark-theme-accent;
    box-shadow: 0.15rem 0.15rem $dark-theme-bg;
    border-radius: 0.2rem;
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
