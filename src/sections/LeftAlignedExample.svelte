<script>
	import { onMount } from "svelte";

	onMount(() => {
		const divElement = document.getElementById("viz1753138395797");
		const vizElement = divElement.getElementsByTagName("object")[0];
		vizElement.style.width = "1244px";
		vizElement.style.height = "627px";

		const scriptElement = document.createElement("script");
		scriptElement.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
		vizElement.parentNode.insertBefore(scriptElement, vizElement);
	});
</script>

<div class="tableauPlaceholder" id="viz1753138395797" style="position: relative">
	<noscript>
		<a href="https://blackwealthdata.org/explore/business">
			<img
				alt="Dashboard - Business Ownership - Section 1.1"
				src="https://public.tableau.com/static/images/3S/3S3T8CMDY/1_rss.png"
				style="border: none"
			/>
		</a>
	</noscript>
	<object class="tableauViz" style="display:none;">
		<param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F" />
		<param name="embed_code_version" value="3" />
		<param name="path" value="shared/3S3T8CMDY" />
		<param name="toolbar" value="yes" />
		<param name="static_image" value="https://public.tableau.com/static/images/3S/3S3T8CMDY/1.png" />
		<param name="animate_transition" value="yes" />
		<param name="display_static_image" value="yes" />
		<param name="display_spinner" value="yes" />
		<param name="display_overlay" value="yes" />
		<param name="display_count" value="yes" />
		<param name="language" value="en-US" />
		<param name="origin" value="viz_share_link" />
		<param name="filter" value="padding=0" />
		<param name="filter" value="position=relative" />
	</object>
</div>
