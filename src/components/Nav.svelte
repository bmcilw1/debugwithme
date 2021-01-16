<script lang="ts">
	export let segment: string;
	let showDropdown = false;
</script>

<nav class='navbar' role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
		<a class="navbar-item logo" href=".">
			<span class="pr-3 is-size-4">🐞</span><strong>DebugWithMe</strong>
		</a>
	
		<!-- svelte-ignore a11y-missing-attribute -->
		<a role="button" on:click="{ () => showDropdown = !showDropdown }" class="navbar-burger { showDropdown ? 'is-active' : ''}" aria-label="menu" aria-expanded="false" data-target="menu">
		  <span aria-hidden="true"></span>
		  <span aria-hidden="true"></span>
		  <span aria-hidden="true"></span>
		</a>
	</div>

	  <div id="menu" class="navbar-menu { showDropdown ? 'is-active' : ''}">
		<div class="navbar-start">
			<a on:click="{() => showDropdown = !showDropdown}" class="navbar-item" aria-current="{segment === undefined ? 'page' : undefined}" href=".">home</a>
			<a on:click="{() => showDropdown = !showDropdown}" class="navbar-item" aria-current="{segment === 'about' ? 'page' : undefined}" href="about">about</a>

			<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
			<a on:click="{() => showDropdown = !showDropdown}" class="navbar-item" rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a>
		</div>
	  </div>
	
</nav>

<style lang="scss">
.logo {
	color: #FA7C91;
}
</style>
