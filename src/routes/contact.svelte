<svelte:head>
    <title>Contact</title>
</svelte:head>
<script>
    import analyticsTracking from '../utils/analytics';
</script>
<style>
    :root{
		--blue: #121f3d;
		--white: #eff3f8;  
	}
    .Contact {
        padding: 0 25% 25% 25%;
        text-align: justify;
        font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
        color: var(--white);
		line-height: 1.5;
    }

    .SocialMedia img {
        width: 35px;
    }
    .SocialMedia {
        padding-bottom: 15px;
        align-self: center;
        display: grid;
        grid-template-columns: 10% auto;
    }
    .SocialMedia__img {
        text-align: center;
    }
    .SocialMedia__title {
        align-self: center;
    }
    .SocialMedia__title a{
        list-style-type: none;
        color: var(--white);
        text-decoration: none;
    }
	@media screen and (max-width: 600px) {
        .Contact {
            padding: 1em;
        }
        .SocialMedia__title {
            padding-left: 15px;
        }
    }
</style>

<div class="Contact">
    <h1>Contact</h1>
    <p>
        If you wanna get in touch or talk about a project, feel free to contact me via email at
        christiantambo15@gmail.com
        .You can also send me a Direct Message on Social Media.
    </p>
    <section class="SocialMedia">
        <div class="SocialMedia__img">
            <a href="https://www.linkedin.com/in/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('linkedin')}>
                <img src="./logo_linkedin.svg" alt="LinkedIn">
            </a>
        </div>
        <div class="SocialMedia__title">
            <a href="https://www.linkedin.com/in/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('linkedin')}>
                LinkedIn
            </a>
        </div>
        
    </section>
    <section class="SocialMedia">
        <div class="SocialMedia__img">
            <a href="https://github.com/ChristianTC" target="_blank" rel="noreferrer" on:click={analyticsTracking('github')}>
                <img src="./logo_github.svg" alt="GitHub">
            </a>
        </div>
        <div class="SocialMedia__title">
            <a href="https://github.com/ChristianTC" target="_blank" rel="noreferrer" on:click={analyticsTracking('github')}>
                GitHub
            </a>
        </div>
        
    </section>
    <section class="SocialMedia">
        <div class="SocialMedia__img">
            <a href="https://twitter.com/ChristianTambo" target="_blank" rel="noreferrer" on:click={analyticsTracking('twitter')}>
                <img src="./logo_twitter.svg" alt="Twitter">
            </a>
        </div>
        <div class="SocialMedia__title">
            <a href="https://twitter.com/ChristianTambo" target="_blank" rel="noreferrer" on:click={analyticsTracking('twitter')}>
                Twitter
            </a>
        </div>
        
    </section>
    <section class="SocialMedia">
        <div class="SocialMedia__img">
            <a href="https://www.instagram.com/christian.jtc/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Instagram')}>
                <img src="./logo_instagram.svg" alt="Instagram">
            </a>
        </div>
        <div class="SocialMedia__title">
            <a href="https://www.instagram.com/christian.jtc/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Instagram')}>
                Instagram
            </a>
        </div>
        
    </section>
    <section class="SocialMedia">
        <div class="SocialMedia__img">
            <a href="https://platzi.com/p/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Platzi')}>
                <img src="./logo_platzi.svg" alt="Platzi">
            </a>
        </div>
        <div class="SocialMedia__title">
            <a href="https://platzi.com/p/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Platzi')}>
                Platzi
            </a>
        </div>
        
    </section>

</div>