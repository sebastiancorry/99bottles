<script>
    // Imports
    import Button from './Button.svelte';

    // State
    let state = 'stock';
    function setSales() {
        state = 'sales';
    }
    function setStock() {
        state = 'stock';
    }
</script>

<div class="main-content">
    <Button on:click="setStock">
        <p>Stock</p>
    </Button>

    <Button on:click="setStock">
        <p>Sales</p>
    </Button>
</div>

<style>
    .main-content{
        /* Colors */
        background-color: #FFFFF0;

        /* Miscellaneous properties */
        overflow: auto;

        /* Dimensions */
        min-height: 95vh;
        max-height: 100vh;
        max-width: 80vw;

        /* Rounded corners */
        border-radius: 5px;
        padding: 20px;

        /* Position */
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }
</style>
