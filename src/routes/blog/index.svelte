<script context="module" lang="ts">
  export function preload() {
    return this.fetch(`blog.json`)
      .then((r: { json: () => any }) => r.json())
      .then(
        (posts: { slug: string; title: string; date: Date; html: any }[]) => {
          return { posts };
        }
      );
  }
</script>

<script lang="ts">
  export let posts: { slug: string; title: string; date: Date; html: any }[];
</script>

<h1>Recent posts</h1>

<ul>
  {#each posts as post}
    <!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->
    <li>
      <a rel="prefetch" href="blog/{post.slug}">{post.title}</a><br />
      <span>Posted on {new Date(post.date).toLocaleDateString()}</span>
    </li>
  {/each}
</ul>
