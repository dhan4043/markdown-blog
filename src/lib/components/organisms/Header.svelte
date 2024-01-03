<!-- Header.svelte -->
<header>
  <a href="/">david han</a>

  <nav>
    <ul>
      <li>
        <a href="/blog">blog</a>
      </li>
      <li>
        <a href="/about">about</a>
      </li>
    </ul>
  </nav>
</header>

<!-- Component Styling -->
<style>

  header {
    padding: 1rem;
    background: #fffff5;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  ul {
    margin: 0;
    list-style-type: none;
    display: flex;
    gap: 1rem;
  }

  a {
    text-decoration: none;
    color: #000;
  }
</style>
