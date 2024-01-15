<!-- Footer.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte'; 
</script>

<footer>
  <hr>
  <nav>
    <ul>
      <li> 
        <a href="/rss">
          <Icon name='rss' width='1rem' height='1.5rem'/>
        </a>
      </li>
      <li> 
        <a href="/github">
          <Icon name='github' width='1rem' height='1.5rem'/>
        </a>
      </li>
      <li> 
        <a href="/">
          <Icon name='home' width='1rem' height='1.5rem'/>
        </a>
      </li>
    </ul>
  </nav>
  <p>made with sveltekit</p>
</footer>

<!-- Component Styling -->
<style lang="scss">
  @import "../../styles/themes.scss";

  :global(body) footer {
    margin: 0;
    margin-bottom: 1rem;
    padding-top: 0;
    background: $light-theme-bg;
    display: block;
    /* flex-wrap: wrap; */
    justify-content: space-between;
    font-size: 1rem;
    line-height: 1.5rem;
  }

  :global(body.dark) footer {
    background: $dark-theme-bg;
  }

  hr {
    border: 0;
    border-bottom: thin solid #ccc;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    gap: 1rem;
  }

  :global(body) a {
    text-decoration: none;
    color: $light-theme-text; 
  }

  :global(body.dark) a {
    color: $dark-theme-text;
  }

  :global(body) p {
    margin: 0;
    padding: 0;
    color: $light-theme-text;
    display: flex;
    flex-wrap: wrap;
  }

  :global(body.dark) p {
    color: $dark-theme-text;
  }
</style>
