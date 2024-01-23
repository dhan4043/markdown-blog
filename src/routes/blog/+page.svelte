<!-- src/routes/blog/+page.svelte -->
<script>
  import BlogCard from '$lib/components/molecules/BlogCard.svelte';
  export let data;
</script>

<!-- <h1>This is my blog!</h1> -->

<ul>
  {#each data.posts as post}
    <li>
      <BlogCard title={post.meta.title} slug={post.path} excerpt={post.meta.date} tags={post.meta.tags}/>
    </li>
    <!-- <li> -->
    <!--   <h2> -->
    <!--     <a href={post.path}> -->
    <!--       {post.meta.title} -->
    <!--     </a> -->
    <!--   </h2> -->
    <!--   Published {post.meta.date} -->
    <!-- </li> -->
  {/each}
</ul>

<style>
  ul {
    margin-left: auto;
    margin-right: auto;
    width: 85%;
    padding: 0;
    list-style-type: none;
    gap: 1rem;
  }

  li {
    margin-bottom: 1rem;
  }
</style>

