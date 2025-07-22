<script>
    import "highcharts/modules/exporting";
    import Scroller from "../lib/Scroller.svelte";
    import ObservedArticleText from "../lib/ObservedArticleText.svelte";

    let hasAlerted = false;

    const options = {
        threshold: [0.85, 0.95],
    };

    const simpleCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                // "active" state
                elem.style.backgroundColor = "#e3ff00";
            } else if (entry.intersectionRatio < 0.9) {
                // "inactive" state
                elem.style.backgroundColor = "#888888";
            }
        });
    };

    const alertCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;
            if (entry.intersectionRatio >= 0.9 && !hasAlerted) {
                // "active" state
                alert(
                    "The first time that article text section scrolls into view," +
                        " this alert pops up! Then, we set the hasAlerted flag to true," +
                        " which we use to prevent the alert from showing again." +
                        " Refresh the page if you want to see it happen again. " +
                        '(btw, "flag" is just a jargon term for a boolean variable!)',
                );
                hasAlerted = true;
            }
        });
    };
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <div>
                <p>
                    📊 This data is from the Black Wealth Data Center 
                    <a
                        href="https://blackwealthdata.org/wealth-indicator?firstCounty=Cumberland%20County,%20North%20Carolina&secondCounty=national&method=auto"
                    >Black Wealth Data Center</a
                    > website
                        </p>

                <p>
                    📍 Location: North Carolina
                </p>
                <p>
                    This chart displays the percentage of business ownership by race across the United States. It highlights the stark disparities in Black business ownership compared to other racial groups, underscoring the persistent wealth and opportunity gaps in entrepreneurship.
                </p>
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ObservedArticleText callback={alertCallback} {options}>
                Racial disparities in business ownership, Black Americans remain significantly underrepresented compared to other groups, reflecting broader systemic inequities in access to capital and opportunities.
            </ObservedArticleText>

            <ObservedArticleText callback={alertCallback} {options}>
                Ultimately, addressing these gaps is essential for building a more just and inclusive economy.
            </ObservedArticleText>

            <ObservedArticleText callback={alertCallback} {options}>
                    Thank you!
            </ObservedArticleText>
        {/snippet}
    </Scroller>
</div>
