
<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<script>
	import Post from '../components/Post.svelte';
	export let posts;
</script>
<style>
	.perfil__container {
		font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
		text-align: center;
	}
	.perfil__container img {
		width: 255px;
		border: white solid 5px;
		border-radius: 100%;
        box-shadow: 0 8px 16px 0 rgba(250,250,250,0.4);
	}
	
	.perfil__container figcaption{
		padding-top: 15px;
		font-family: OCR A Std, monospace;
		color: #eff3f8;
		font-size:xx-large;
	}
	.perfil__content {
		margin-left: 100px;
		margin-right: 100px;
		padding-top: 15px;
		/* margin: 50px; */
		font-family: sans-serif;
		color: #eff3f8;
		font-size:medium;
		text-align: justify;
		line-height: 2;
	}
	.perfil__content p {
		text-align: center;
    }
	.perfil__content a {
		text-decoration: none;
		color: #eff3f8;

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

	@media screen and (max-width: 600px) {
        .perfil__content {
			margin-left: 50px;
			margin-right: 50px;
			padding-top: 15px;
			/* margin: 50px; */
			font-family: sans-serif;
			color: #eff3f8;
			font-size:medium;
			text-align: justify;
			line-height: 2;
        }

		.Posts {
			
			padding: 0;
			display: grid;
			justify-content: space-between;
			grid-gap: 15px;
			grid-template-columns: 1fr;
		}
    }
</style>

<section class="perfil__container">
	<figure>
		<img src="./fotoperfil.jpg" alt="I'm Christian Tambo">
		<figcaption>Hi, I'm Christian Tambo</figcaption>
	</figure>

	<section class="perfil__content">
		<a aria-current href="portfolio">
			<p>
				Check out my projects I have recently been working on 		
			</p>
		</a>
		
	</section>
	
</section>

<section class="Posts">
	Recent posts
	{#each posts as post}
		<Post {post} />
	{/each}
</section>
