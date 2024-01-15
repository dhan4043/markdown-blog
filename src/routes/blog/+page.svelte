<!-- src/routes/blog/+page.svelte -->
<script>
  import BlogCard from '$lib/components/molecules/BlogCard.svelte';
  export let data;
</script>

<h1>This is my blog!</h1>

<ul>
  {#each data.posts as post}
    <BlogCard title={post.meta.title} slug={post.path}/>
    <li>
      <h2>
        <a href={post.path}>
          {post.meta.title}
        </a>
      </h2>
      Published {post.meta.date}
    </li>
  {/each}
</ul>

