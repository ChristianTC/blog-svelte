<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	import Post from '../../components/Post.svelte';
	export let posts;
</script>

<style>
	:root{
		--blue: #121f3d;
		--white: #eff3f8;  
	}
	.Posts {			
		color: #eff3f8;

		font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
		padding: 0 10% 10% 10%;
		display: grid;
		justify-content: space-between;
		grid-gap: 15px;
		grid-template-columns: 1fr;
	}
	
</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>


<section class="Posts">
	<h1>Recent posts</h1>
	{#each posts as post}
		<!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->
		<Post {post} />
		<!-- <li><a rel="prefetch" href="blog/{post.slug}">{post.title}</a></li> -->
	{/each}
</section>
