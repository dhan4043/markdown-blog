<!-- Header.svelte -->
<script>
  import Icon from '$lib/components/atoms/Icon.svelte'; 
  import ThemeSwitch from '$lib/components/molecules/ThemeSwitch.svelte';
</script>

<header>
  <nav>
    <ul>
      <li>
        <a href="/">david han</a>
      </li>
      <li>
        <span>|</span>
      </li>
      <li>
        <a href="/blog">blog</a>
      </li>
      <li>
        <a href="/about">about</a>
      </li>
      <li>
        <a href="/contact">contact</a>
      </li>
      <li>
        <ThemeSwitch width="1.4rem" height="1.4rem"/>
      </li>
      <li>
        <Icon name='more-horizontal' width='1.4rem' height='2.1rem'/>
      </li> 
    </ul>
  </nav>
</header>

<!-- Component Styling -->
<style lang="scss">
  @import "../../styles/themes.scss";
  :global(body) header {
    margin: 0;
    padding-top: 2rem;
    padding-right: 0;
    padding-bottom: 0;
    padding-left: 0;
    background: $light-theme-bg;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;   
    align-content: start;
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

  ul li:first-child {
    font-weight: bold;
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
