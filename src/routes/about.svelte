<svelte:head>
	<title>About</title>
	<link rel="stylesheet" href="../assets/styles/about.css">
</svelte:head>

<style>

	:root{
		--blue: #121f3d;
		--white: #eff3f8;  
	}

	.About__container {
		display: grid;
		grid-template-columns: 40% auto;
		text-align: center;
		margin: 0;
		
	}
	.About-me {
		padding-right: 30%;
	}
	.About-me-description {
		font-family: "Saira",sans-serif;
	}
	.About__container figure {
		padding-top: 35px;
		text-align: end;
	}
	.About__container img {
		width: 120px;
		border: white solid 2px;
		border-radius: 100%;
        box-shadow: 0 8px 16px 0 rgba(250,250,250,0.4);
	}
	.About__container h1{
		font-family: sans-serif;
		color: var(--white);
	}
	.About__container p{
		font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
		color: var(--white);
		line-height: 1.5;
		text-align: justify;
	}
	.About__details {
		font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
	}
	.About__details--section {
		text-align: center;
		font-size: xx-large;
		color: var(--white);	
	}
	.About__details--description {
		font-family: Arial, Helvetica, sans-serif;	
		color: var(--white);
		
		padding-top: 10px;
		display: grid;
		grid-template-columns: 50% auto;	
	}
	.About__details--title {
		font-family: 'Courier New', Courier, monospace;
		font-size: x-large;
		align-self: center;
		font-weight: bold;
		text-align: end;
	}
	.About__details--content ul{
		font-family: "Saira",sans-serif;
		letter-spacing: 0.1em;
	}

	

	

	
	@media screen and (max-width: 600px) {
		.About__container {
			display: grid;
			grid-template-columns: auto;
			text-align: center;
			margin: 0;
		}
		.About__container figure {
			padding-top: 0;
		}
		.About-me {
			padding-right: 0;
		}
		.About__container figure {
			padding-top: 35px;
			text-align: center;
		}
	}
</style>

<section class="About__container">
	<div class="About">
		
		<figure>
			<img src="./fotoperfil.jpg" alt="I'm Christian Tambo">
		</figure>

		
	</div>
	<div class="About-me">
		<h1>ABOUT ME</h1>
		<article class="About-me-description">
			<p>
				Hi!, first of all I want to thank you for visiting my personal website.			
			</p>
			<p>
				My name is Christian Tambo, I'm a developer from Bolivia, who is mainly interested in web technologies, now I'm focused in Front-end Development.
			</p>
		</article>
	</div>
</section>
<section class="About__details">
	<p class="About__details--section">
		KNOWLEDGE
	</p>
	<hr>
	<div class="About__details--description">
		<section class="About__details--title">
			Languages
		</section>
		<section class="About__details--content">
			<ul>
				<li>JavaScript</li>
				<li>Python</li>
				<li>C, C++</li>
				<li>PHP</li>
				<li>HTML</li>
				<li>CSS</li>
			</ul>
		</section>
		<section class="About__details--title">
			Frameworks
		</section>
		<section class="About__details--content">
			<ul>
				<li>React</li>
				<li>Angular</li>
				<li>Svelte</li>
			</ul>
		</section>
		<section class="About__details--title">
			Databases
		</section>
		<section class="About__details--content">
			<ul>
				<li>MySQL</li>
			</ul>
		</section>
		<section class="About__details--title">
			Control Version
		</section>
		<section class="About__details--content">
			<ul>
				<li>Git</li>
				<li>GitHub</li>
			</ul>
		</section>
	</div>
</section>
