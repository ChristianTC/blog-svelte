<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>

<style>
    .project__container {
        display: grid;
        grid-template-columns: 50% auto;
        width: 800px;
    }
    .project__content {
        text-align: center;
        width: 100%;
    }
    .project__content img{
        border: solid bisque 0.2px;
        border-radius: 15px;
        cursor: pointer;
        height: 300px;
        margin-top: 30px;
        width: 95%;
    }
    .project__content img:hover{
        border: solid bisque 1px;
    }
    .project__button {
        background-color: bisque;
        border-radius: 25px;
        color: #31449b;
        cursor: pointer;
        font-family: "Saira",sans-serif;
        font-weight: bold;
        letter-spacing: 0.1em;
        margin-left: 25%;
        margin-top: 1px;
        padding: 5px;
        text-align: center;
        text-decoration: none;
        width: 50%;
    }
    .project__button a {
        color: #31449b;
        text-decoration: none;
    }
    .project__button a:hover {
        color: white;
    }
    .project__button:hover{
        background-color: #31449b;
        color: white;
    }
    .project__technologies {
        color: bisque;
        font-family: "Saira",sans-serif;
        font-size: small;
        font-weight: bold;
        letter-spacing: 0.1em;
        margin-left: 10%;
        margin-top: 1px;
        padding: 5px;
        text-align: center;
        width: 80%;
    }
	@media screen and (max-width: 800px) {
    
        .project__container {
            display: grid;
            grid-template-columns: auto;
            width: 350px;
        }

    }
</style>

<script>
    import Post from '../components/Post.svelte';
    export let posts;
    const filterPost = posts.filter(post => post.tag === 'general');
</script>

<svelte:head>
    <title>
        General
    </title>
</svelte:head>


<section class="project__container">
    <section class="project__content">
        <a target="_blank" href="https://christiantambo.netlify.app/">
            <img src="./project2.png" alt="">
        </a>
            <div class="project__button">
                <a target="_blank" href="https://christiantambo.netlify.app/">
                    VIEW PAGE 🢅
                </a>
            </div>
            <div class="project__technologies">
                SVELTE / HTML / CSS / JS
            </div>
    </section>
    <section class="project__content">
        <a target="_blank" href="https://www.supercontrato.com/">
            <img src="./project1.png" alt="">
        </a>
        <div class="project__button">
            <a target="_blank" href="https://www.supercontrato.com/">
            VIEW PAGE 🢅
            </a>
        </div>
        <div class="project__technologies">
            WORDPRESS
        </div>
    </section>
    <section class="project__content">
    </section>
</section>