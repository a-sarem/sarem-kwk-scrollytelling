<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="duck-img" src="duck.png" alt="KWK rubber duck!" />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                    This chart breaks down the racial composition of business ownership in Cumberland County, NC. It reveals that Black-owned businesses represent a significantly smaller share compared to those owned by White and other racial groups, despite Black residents forming a substantial part of the population.
            </ArticleText>

            <ArticleText>This disparity underscores the systemic barriers (i.e. unequal access to capital, mentorship, and networks), that continue to limit Black entrepreneurship. Highlighting these imbalances is crucial for understanding and addressing racial inequity in local economic opportunities.</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .duck-img {
        width: 25%;
        margin: 0px auto;
    }
</style>
