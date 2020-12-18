<script>
	import Sidebar from './Sidebar.svelte';

</script>

<style>
    
    .Main-container {
        padding-bottom: 100px;
        display: grid;
        grid-template-columns: minmax(auto, 1024px);
        justify-content: center;
        align-items: center;
    }

    .Main-content {
        margin: 2em 0 0 0;
        display: grid;
        /* grid-template-columns: 5fr 0fr; */
        grid-gap: 60px;
        justify-content: space-between;
    }
    
</style>

<main>
    <div class="Main-container">
        <div class="Main-content">
            <slot />
            <Sidebar />
            
        </div>
    </div>
</main>