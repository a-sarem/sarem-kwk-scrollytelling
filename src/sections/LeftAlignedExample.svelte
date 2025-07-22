<script>
  import { onMount } from "svelte";

  onMount(() => {
    const divEl = document.getElementById("viz-business-race");
    const viz = divEl.getElementsByTagName("object")[0];

    // Keep your original sizing but adjust slightly
    viz.style.width = "700px";
    viz.style.height = "580px";

    const script = document.createElement("script");
    script.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
    viz.parentNode.insertBefore(script, viz);
  });
</script>

<div style="display: flex; gap: 30px; align-items: flex-start; max-width: 1400px;">
  <!-- Left section with Tableau viz -->
  <div
    class="tableauPlaceholder"
    id="viz-business-race"
    style="
      position: relative; 
      width: 700px; 
      height: 580px;
      overflow: hidden;
      border: 1px solid #ddd;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.15);
      flex-shrink: 0;
    "
  >
    <noscript>
      <a href="https://public.tableau.com/shared/3S3T8CMDY">
        <img
          alt="Business Ownership by Race"
          src="https://public.tableau.com/static/images/3S/3S3T8CMDY/1_rss.png"
          style="border: none; width: 700px; height: 580px;"
        />
      </a>
    </noscript>
    <object class="tableauViz" style="display:none;">
      <param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F"/>
      <param name="embed_code_version" value="3"/>
      <param name="path" value="shared/3S3T8CMDY"/>
      <param name="toolbar" value="no"/>
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

  <!-- Right section with your text content -->
  <div style="flex: 1; min-width: 300px;">
    <div style="background: #f8f9fa; padding: 24px; border-radius: 8px; border: 1px solid #e9ecef;">
      <h3 style="margin-top: 0; color: #2c3e50;">Business Ownership Analysis</h3>
      <p style="line-height: 1.6; margin-bottom: 20px;">
        This visualization shows the distribution of employer firms by receipt amount, 
        broken down by race and ethnicity. The data reveals important patterns in 
        business ownership and economic participation across different demographic groups.
      </p>
      
      <h4 style="color: #34495e; margin-bottom: 12px;">Key Insights:</h4>
      <ul style="line-height: 1.6; padding-left: 20px;">
        <li style="margin-bottom: 8px;">Most firms fall within the $25,000 to $49,999 receipt range</li>
        <li style="margin-bottom: 8px;">There are significant disparities in business ownership across racial groups</li>
        <li style="margin-bottom: 8px;">The data reflects broader economic inequalities in business access and success</li>
      </ul>
      
      <p style="margin-top: 20px; font-style: italic; color: #6c757d;">
        <small>Data Source: Black Wealth Data Center, 2023</small>
      </p>
    </div>
  </div>
</div>

<style>
  /* Gentle approach to reduce white space without breaking functionality */
  .tableauPlaceholder iframe {
    transform: translateY(-20px); /* Move content up slightly to crop top white space */
  }
  
  /* Alternative: if there's white space on the sides */
  .tableauPlaceholder {
    /* Uncomment if you need to crop sides:
    clip-path: inset(20px 0px 40px 0px);
    */
  }
</style>