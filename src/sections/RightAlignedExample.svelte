<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "column",
    },
    title: {
      text: "PPP Loan Approval Amount per Black Capita (2020-2021)",
    },
    plotOptions: {
      pie: {
        allowPointSelect: true,
        dataLabels: [
          {
            enabled: true,
            distance: 20,
          },
          {
            enabled: true,
            distance: -40,
            format: "{point.percentage:.1f}%",
            style: {
              fontSize: "1.2em",
              textOutline: "none",
            },
            filter: {
              operator: ">",
              property: "percentage",
              value: 10,
            },
          },
        ],
      },
    },
    series: [
      {
        name: "Cumberland County (North Carolina)",
        data: [
          {
            name: "Cumberland County (North Carolina)",
            y: 192,
          },
          {
            name: "National",
            sliced: true,
            selected: true,
            y: 441
          },
        ],
      },
    ],
  };
</script>


<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
      <p>
       📊 This data is from the Black Wealth Data Center 
        <a
          href="https://blackwealthdata.org/wealth-indicator?firstCounty=Cumberland%20County,%20North%20Carolina&secondCounty=national&method=auto"
          >Black Wealth Data Center</a
        > website
      </p>
      <p>
        📍 <strong>Location: </strong>  Cumberland County, North Carolina. 
        all kinds of charts.
      </p>
      <p>
        This data displays Cumberland Countys' loan approval for black owned businesses. The blue column represents Cumberland County, while the grey column represents the national.
      </p>
      <p>
        The data can uncover inequities in business support, particularly for Black-owned businesses in specific counties, such as Cumberland County, North Carolina, compared to the national average.
      </p>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        Racial wealth disparities are a core challenge in the U.S. economy. This
        project explores how economic opportunities differ for Black
        communities.
      </ArticleText>

      <ArticleText>
        This data shows how acsess to capital was not equal. During COVID-19, <strong
          >PPP Loans</strong
        > (a federal funding program to support small businesses through COVID-19) was not distributed
        equally.
      </ArticleText>

      <ArticleText>
        Additonally, this reflects access to emergency small business loans and highlights the disparities in how financial relief distributed. 
      </ArticleText>

    {/snippet}
  </Scroller>
</div>

<style>
  .chart {
    width: 90%;
    margin: 0px auto;
  }
</style>
