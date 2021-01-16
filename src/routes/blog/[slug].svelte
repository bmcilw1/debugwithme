<script context="module" lang="ts">
  export async function preload({ params }) {
    // the `slug` parameter is available because
    // this file is called [slug].svelte
    const res = await this.fetch(`_posts/${params.slug}.md`);

    if (res.status === 200) {
      return { postMd: await res.text() };
    } else {
      this.error(res.status, res.data.message);
    }
  }
</script>

<script lang="ts">
  import fm from "front-matter";
  import MarkdownIt from "markdown-it";

  export let postMd: string;

  const md = new MarkdownIt();

  $: frontMatter = fm(postMd);
  $: post = {
    title: frontMatter.attributes["title"],
    html: md.render(frontMatter.body),
  };
</script>

<section class="section">
  <div class="container">
    <h1 class="title is-2">{post.title}</h1>

    <div class="content">
      {@html post.html}
    </div>
  </div>
</section>
