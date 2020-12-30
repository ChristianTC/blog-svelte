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
	.Post, .Post h2 {
		color: var(--white);
		font-family: sans-serif;
		letter-spacing: 0.1em;
		text-align: justify;

	}
	.Post p {
		font-size: 14px;
		font-weight: 300;
		margin-top: 5px;
		padding: 0;
	}
	.comments {
		margin: 2em 0 0 0;
	}
	@media screen and (max-width: 600px) {
		.Post {
			padding-left: 0;
			padding-right: 0;
		}

	}

</style>


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
	<div class="content">
		{@html post.html}
	</div>
	<div class="comments">
		<div id="disqus_thread">
			
		</div>
	</div>

</div>

