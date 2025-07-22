<script>
  import { onMount } from "svelte";

  onMount(() => {
    const divEl = document.getElementById("viz-business-race");
    const viz = divEl.getElementsByTagName("object")[0];
    viz.style.width = "350px";
    viz.style.height = "300px";

    const script = document.createElement("script");
    script.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
    viz.parentNode.insertBefore(script, viz);
  });
</script>

<div
  class="tableauPlaceholder"
  id="viz-business-race"
  style="position: relative; float: left; margin-right: 20px;"
>
  <noscript>
    <a href="https://public.tableau.com/shared/3S3T8CMDY">
      <img
        alt="Business Ownership by Race"
        src="https://public.tableau.com/static/images/3S/3S3T8CMDY/1_rss.png"
        style="border: none; width: 350px; height: 300px;"
      />
    </a>
  </noscript>
  <object class="tableauViz" style="display:none;">
    <param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F"/>
    <param name="embed_code_version" value="3"/>
    <param name="path" value="shared/3S3T8CMDY"/>
    <param name="toolbar" value="yes"/>
    <param name="static_image" value="https://public.tableau.com/static/images/3S/3S3T8CMDY/1.png"/>
    <param name="animate_transition" value="yes"/>
    <param name="display_static_image" value="yes"/>
    <param name="display_spinner" value="yes"/>
    <param name="display_overlay" value="yes"/>
    <param name="display_count" value="yes"/>
    <param name="language" value="en-US"/>
    <param name="origin" value="viz_share_link"/>
  </object>
</div>