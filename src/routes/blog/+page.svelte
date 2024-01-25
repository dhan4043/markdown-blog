<!-- src/routes/blog/+page.svelte -->
<script>
  import BlogCard from '$lib/components/molecules/BlogCard.svelte';
  import Pagination from '$lib/components/atoms/Pagination.svelte';
  export let data;
  let posts;
</script>

<h1>Posts</h1>

{#if posts}
{#each posts as post}
<p>
  <BlogCard title={post.meta.title} slug={post.path} excerpt={post.meta.date} tags={post.meta.tags}/>
</p>
{/each}
{/if}
<Pagination rows={data.posts} perPage={3} bind:trimmedRows={posts} />
<!-- <h1>This is my blog!</h1> -->

<!-- <ul> -->
<!--   {#each data.posts as post} -->
<!--     <li> -->
<!--       <BlogCard title={post.meta.title} slug={post.path} excerpt={post.meta.date} tags={post.meta.tags}/> -->
<!--     </li> -->
<!--     <li> -->
<!--       <h2> -->
<!--         <a href={post.path}> -->
<!--           {post.meta.title} -->
<!--         </a> -->
<!--       </h2> -->
<!--       Published {post.meta.date} -->
<!--     </li> -->
<!--   {/each} -->
<!-- </ul> -->

<style>
  ul {
    //margin-left: auto;
    //margin-right: auto;
    //width: 85%;
    padding: 0;
    list-style-type: none;
    gap: 1rem;
  }

  li {
    margin-bottom: 1rem;
  }
</style>

