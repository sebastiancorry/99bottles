<script>
    // Imports
    import Button from './Button.svelte';

    // State
    let state = 'stock';
    function setStock() {
        state = 'stock';
    }
    function setSales() {
        state = 'sales';
    }
</script>

<div class="main-content">
    <!-- Tabs -->
    <Button on:click={setStock}>
        <p>Stock</p>
    </Button>
    <Button on:click={setSales}>
        <p>Sales</p>
    </Button>

    <!-- Content -->
    {#if state === 'stock'} 
        <p>Stock</p>
    {:else if state === 'sales'}
        <p>Sales</p>
    {:else}
        <p>ERROR: Unknown state</p>
    {/if}
</div>

<style>
    .main-content{
        /* Color */
        background-color: #FFFFF0;

        /* Miscellaneous properties */
        overflow: auto;

        /* Dimensions */
        min-height: 95vh;
        max-height: 100vh;
        max-width: 80vw;

        /* Shape */
        border-radius: 5px;
        padding: 20px;

        /* Position */
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }
</style>
