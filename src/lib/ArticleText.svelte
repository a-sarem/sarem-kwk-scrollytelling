<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 50%;
        background-color: #5d5bb9;
        color: white;
        font-family: 'Courier New', Courier, monospace;
        border: solid black 1px;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 16px 16px #260f62;
    }
</style>
