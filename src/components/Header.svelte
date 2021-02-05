<script>
    import analyticsTracking from '../utils/analytics';
</script>

<style>
    .Header {
        /* background-color: #000; */
        color: #191a22;
        padding: 0 0 0 0;
    }
    .Header-container {
        display: grid;
        grid-template-columns: minmax(auto, 1024px);
        justify-content: center;
        align-items: center;
    }
    .Header-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .Header h1 {
        margin-left: 5px;
        color: #eff3f8;
        font-size: 20px;
        font-weight: 700;
        letter-spacing: 0.8px;
        cursor: pointer;
        font-family: sans-serif;
    }
    .Header h1 span {
        color: #eff3f8;
        display: block;
        font-size: 13px;
        font-weight: 300;
        letter-spacing: normal;
        margin: 0.3em 0 0 0;
        font-family: Arial, Helvetica, sans-serif;
    }
    .Header ul {
        padding: 0;
        list-style: none;
    }
    .Header li {
        display: inline-block;
        margin: 0 0.5em 0 0;
    }
    .Header a { 
        text-decoration: none;
        font-weight: 300;
        font-size: 14px;
    }
    .Header-social img {
        width: 20px;
    }
    .img_round {
        background: rgb(255,255,255);
        background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 16%, rgba(0,0,0,1) 100%);
        border-radius: 100%;
    }

    .Header-logo {
        display: flex;
    }
    /* .Header-logo-rounded {
        align-self: center;
        padding: 15px;
        color: #eff3f8;
        font-size: 20px;
        font-weight: 700;
        letter-spacing: 0.8px;
        cursor: pointer;
        font-family: sans-serif;
        border: solid 1px #fff;
        border-radius: 100%;

        box-shadow: inset  8px 16px 0 rgba(250,250,250,0.4),
		inset 8px 16px 0 #00f;
		
		animation: animate 5s linear infinite;
    } */

    @keyframes animate{
        0% {
            filter: hue-rotate(0deg);
        }
        100% {
            filter: hue-rotate(360deg);
        }
	}

    
</style>

<header class="Header">
    <div class="Header-container">
        <div class="Header-content">
            <div class="Header-logo">
                <a href="/">
                    <h1>
                        Christian Tambo
                        <span>Software Engineer</span>
                    </h1>
                </a>
            </div>
            <div class="Header-social">
                <ul>
                    <li>
                        <a href="https://www.linkedin.com/in/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('linkedin')}>
                            <img src="./logo_linkedin.svg" alt="LinkedIn">
                        </a>
                    </li>
                    <li>
                        <a href="https://github.com/ChristianTC" target="_blank" rel="noreferrer" on:click={analyticsTracking('github')}>
                            <img class="img_round" src="./logo_github.svg" alt="GitHub">
                        </a>
                    </li>
                    <li>
                        <a href="https://twitter.com/ChristianTambo" target="_blank" rel="noreferrer" on:click={analyticsTracking('twitter')}>
                            <img src="./logo_twitter.svg" alt="Twitter">
                        </a>
                    </li>
                    <li>
                        <a href="https://www.instagram.com/christian.jtc/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Instagram')}>
                            <img src="./logo_instagram.svg" alt="Instagram">
                        </a>
                    </li>
                    <li>
                        <a href="https://www.platzi.com/p/christiantambo/" target="_blank" rel="noreferrer" on:click={analyticsTracking('Instagram')}>
                            <img src="./logo_platzi.svg" alt="Platzi">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</header>