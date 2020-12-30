<style>
    .Footer {
        background: rgba(28, 41, 56,0.8);
        color: white;
        padding: 0.5em 0;
        margin: 2em 0 0 0;
        font-size: 13px;
        font-weight: 300;
        
        position: fixed;
        left: 0;
        bottom: 0;
        width: 100%;
        color: white;
        text-align: center;
    }
    .Footer-container {
        display: grid;
        grid-template-columns: minmax(auto, 1024px);
        align-items: center;
        justify-content: center;
    }
    .Footer-content {
        font-family: sans-serif;
        padding-left: 15px;
        padding-right: 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .Footer-svelte {
        display: flex;
        align-self: center;
    }
    .Footer-svelte img {
        width: 50px;
        margin: 0 0 0 0.5em;
    }


    @media screen and (max-width: 600px){
        .Footer {
            background: rgba(28, 41, 56,1);
            color: white;
            padding: 0.5em 0;
            margin: 2em 0 0 0;
            font-size: 10px;
            font-weight: 300;
            
            position: fixed;
            left: 0;
            bottom: 0;
            width: 100%;
            text-align: center;
        }
        .Footer-svelte img {
            width: 25px;
            margin: 0 0 0 0.5em;
        }
    } 

</style>

<footer class="Footer">
    <div class="Footer-container">
        <div class="Footer-content">
            <div class="Footer-copy">
                Developed by Christian Tambo 
            </div>
            <div class="Footer-svelte">
                <!-- Proudly powered by svelte -->
                <img src="logo-192.png" alt="Svelte">
            </div>
        </div>
    </div>
</footer>