<script context="module">
	export async function preload({ params }) {
		// the `slug` parameter is available because
		// this file is called [slug].svelte
		const res = await this.fetch(`blog/${params.slug}.json`);
		const data = await res.json();

		if (res.status === 200) {
			return { post: data };
		} else {
			this.error(res.status, data.message);
		}
	}
</script>

<script>
	import readingTime from "../../utils/readingTime";
	import formatIsoTime from '../../utils/formatIsoTime';
	import { onMount } from "svelte";

	export let post;


	const disqus = () => {
	
		if(document.readyState === 'complete') {
			let d = document, s = d.createElement('script');
			s.src = 'https://chrisdev-1.disqus.com/embed.js';
			s.setAttribute('data-timestamp', +new Date());
			(d.head || d.body).appendChild(s);
		}
    };

	onMount(async () => {
		await disqus();
	});

</script>

<style>
	:root{
		--blue: #121f3d;
		--white: #eff3f8;  
	}
	h2 {
		color: #22215b;
		font-size: 28px;
		margin: 0;
		padding: 0;
	}
	/* .Post {
		padding-left: 15%;
		padding-right: 15%;
	} */
	
	.Post__container {
		max-width: 800px;
		padding: 20px;
	}

	.Post, .Post h2 {
		color: var(--white);
		letter-spacing: 0.1em;
		
	}
	.Post p {
		text-align: justify;
		font-size: 11px;
		font-weight: 300;
		margin-top: 5px;
		padding: 0;
		color: var(--white);
	}
	.Post img {
		width: 600px;
		border-radius: 20px;
	}
	.comments {
		margin: 2em 0 0 0;
	}
	.date {
		text-align: start;
	}
	
	.image {
		text-align: center;
	}
	
	
	@media screen and (max-width: 700px) {
		.Post__container {
			width: 80%;
		}
		.Post img {
			width: 300px;
		}
		.Post {
			text-align: justify;
		}
	}
	@media screen and (max-width: 400px) {
		.Post__container {
			width: 300px;
		}
		.Post img {
			width: 250px;
		}
		.Post {
			text-align: justify;
		}
	}
	

</style>
<link rel="stylesheet" href="./globals.css">
<!-- {post.title}
<time datatime="post.createdAt">
	📅 {formatIsoTime(post.createdAt)}
</time>
<span>{readingTime(post.html)}</span>
<div id="disqus_thread">
				
</div> -->
<svelte:head>
    <meta property="og:title" content="European Travel Destinations">
	<meta property="og:description" content="Offering tour packages for individuals or groups.">
	<meta property="og:image" content="http://euro-travel-example.com/thumbnail.jpg">
	<meta property="og:url" content="http://euro-travel-example.com/index.htm">
</svelte:head>

<div class="Post__container">
	<div class="Post">
		<div class="Post-title">
			<h2>{post.title}</h2>
		</div>
		<p class="date">
			<time datatime="post.createdAt">
				📅 {formatIsoTime(post.createdAt)}
			</time>
			<span>{readingTime(post.html)}</span>
			
		</p>
		<figure class="image">
			<img src="{post.image}" alt="">
		</figure>
		<div class="content">
			{@html post.html}
		</div>
		<div class="comments">
			<div id="disqus_thread">
				
			</div>
		</div>
		
	</div>
		
</div>

