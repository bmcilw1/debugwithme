<script lang="ts">
  export let segment: string;
  let showDropdown = false;
</script>

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item logo" href=".">
      <img src="/favicon.ico" alt="logo" /><strong class="pl-2"
        >DebugWithMe</strong
      >
    </a>

    <!-- svelte-ignore a11y-missing-attribute -->
    <a
      role="button"
      on:click={() => (showDropdown = !showDropdown)}
      class:is-active={showDropdown}
      class="navbar-burger"
      aria-label="menu"
      aria-expanded="false"
      data-target="menu">
      <span aria-hidden="true" />
      <span aria-hidden="true" />
      <span aria-hidden="true" />
    </a>
  </div>

  <div id="menu" class="navbar-menu {showDropdown ? 'is-active' : ''}">
    <div class="navbar-start">
      <a
        on:click={() => (showDropdown = !showDropdown)}
        class="navbar-item"
        aria-current={segment === undefined ? "page" : undefined}
        href=".">Home</a
      >
      <a
        on:click={() => (showDropdown = !showDropdown)}
        class="navbar-item"
        aria-current={segment === "about" ? "page" : undefined}
        href="about">About</a
      >

      <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
      <!-- <a on:click="{() => showDropdown = !showDropdown}" class="navbar-item" rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">Blog</a> -->
    </div>
  </div>
</nav>

<style lang="scss">
  .logo {
    color: #fa7c91;
  }
</style>
