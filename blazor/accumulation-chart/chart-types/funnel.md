---
title: "Funnel Chart in Blazor Accumulation Charts component | Syncfusion"

component: "Accumulation Charts"

description: "Learn here all about Funnel Chart of Syncfusion Accumulation Charts (SfAccumulationChart) component and more."
---

# Funnel Chart

[`Funnel Chart`](https://www.syncfusion.com/blazor-components/blazor-charts/chart-types/funnel-chart) is often used to represent stages in a sales process and show the amount of potential revenue for each stage. To render the [`Funnel Chart`](https://www.syncfusion.com/blazor-components/blazor-charts/chart-types/funnel-chart), set the series [`Type`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Type)
as [`Funnel`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationType.html#Syncfusion_Blazor_Charts_AccumulationType_Funnel).

{% aspTab template="chart/accumulation-charts/funnel/default", sourceFiles="default.razor" %}

{% endaspTab %}

![Funnel Chart](../images/funnel/default-razor.png)

## Funnel Size

The size of the funnel chart can be customized by using the [`Width`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Width) and [`Height`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Height) properties.

{% aspTab template="chart/accumulation-charts/funnel/size", sourceFiles="size.razor" %}

{% endaspTab %}

![Funnel Size](../images/funnel/size-razor.png)

> Note: You can also explore our [`Blazor Funnel Chart`](https://blazor.syncfusion.com/demos/chart/funnel) example to knows how to render and configure the funnel chart.

## Funnel Neck Size

The neck size of the funnel chart can be customized by using the [`NeckWidth`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_NeckWidth) and [`NeckHeight`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_NeckHeight) properties.

{% aspTab template="chart/accumulation-charts/funnel/neck-size", sourceFiles="neck-size.razor" %}

{% endaspTab %}

![Funnel Neck Size](../images/funnel/neck-size-razor.png)

## Gap Between Funnel Segments

[`Funnel chart`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationType.html#Syncfusion_Blazor_Charts_AccumulationType_Funnel) provides options to customize the space between the segments by using the [`GapRatio`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_GapRatio) property of the
series. It accepts values ranging from 0 to 1.

{% aspTab template="chart/accumulation-charts/funnel/gap", sourceFiles="gap.razor" %}

{% endaspTab %}

![Gap Between Funnel Segments](../images/funnel/gap-razor.png)

## Funnel Explode

Points can be exploded on mouse click by setting the [`Explode`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_Explode) property to **true**. You can also explode the point
on load using [`ExplodeIndex`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_ExplodeIndex). Explode distance can be set by using [`ExplodeOffset`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.AccumulationChartSeries.html#Syncfusion_Blazor_Charts_AccumulationChartSeries_ExplodeOffset) property.

{% aspTab template="chart/accumulation-charts/funnel/explode", sourceFiles="explode.razor" %}

{% endaspTab %}

![Funnel Explode](../images/funnel/explode-razor.png)

## Smart Data Label

Labels will be arranged smartly automatically on left side of the funnel and pyramid chart, when they overlaps with each other.

{% aspTab template="chart/accumulation-charts/funnel/smart-data-label", sourceFiles="smart-data-label.razor" %}

{% endaspTab %}

![Smart Data Label](../images/funnel/smart-data-label-razor.png)

> Refer to our [`Blazor Charts`](https://www.syncfusion.com/blazor-components/blazor-charts) feature tour page for its groundbreaking feature representations and also explore our [`Blazor Accumulation Chart Example`](https://blazor.syncfusion.com/demos/chart/funnel?theme=bootstrap4) to know various features of accumulation charts and how it is used to represent numeric proportional data.

## See Also

* [Data label](../data-label/)
* [Grouping](../grouping/)
