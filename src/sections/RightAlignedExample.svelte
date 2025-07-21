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
        This bar chart from the BWDC displays the
        <a
          href="https://blackwealthdata.org/wealth-indicator?firstCounty=Cumberland%20County,%20North%20Carolina&secondCounty=national&method=auto"
          >PPP Loan Approval Amount per Black Capita</a
        >
      </p>
      <p>
        📈 <strong>Highcharts</strong> is a super-flexible library for creating
        all kinds of charts. See demos of different chart types
        <a href="https://www.highcharts.com/demo">here</a>.
      </p>
      <p>
        Since we're using Highcharts through Svelte, the syntax is a little
        different from what you might see in the demos. But all of Highcharts'
        functionality is available through the Highcharts for Svelte package.
      </p>
      <p>
        The configuration is done through the
        <code>options</code> json object passed to the chart, which you'll see in
        the source code for this template.
      </p>
      <p>
        Use the
        <a href="https://api.highcharts.com/highcharts/">API reference</a>
        to understand what each element in the <code>options</code> object does.
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
        > (a program to support small businesses through COVID-19) was not distributed
        equally.
      </ArticleText>

      <ArticleText>
        You can use this template as a <strong>starting point</strong>
        for your project.
        <br /><br />
        Or, if you want to build something from scratch, you can use it as a
        <strong>reference</strong> for specific functionality.
      </ArticleText>

      <ArticleText>
        This is <strong>just one way</strong> that scrollytelling can look.
        <br /><br />
        <strong>
          If you use this template, be sure to modify it and make it your own!
        </strong>
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
