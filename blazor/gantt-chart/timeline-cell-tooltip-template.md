---
layout: post
title: Timeline cell tooltip template in Blazor Gantt Chart Component | Syncfusion
description: Checkout and learn here all about customizing the timeline cell tooltip tasks in Syncfusion Blazor Gantt Chart component and more.
platform: Blazor
control: Gantt Chart
documentation: ug
---

### Timeline cell tooltip

Customizing the timeline cell tooltip in a Gantt Chart using [GanttTooltipSettings.TimelineCellTemplate](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Gantt.GanttTooltipSettings-1.html#Syncfusion_Blazor_Gantt_GanttTooltipSettings_1_TimelineCellTemplate) allows you to display additional information and elements in a more visually appealing and informative way. By combining data bindings and CSS styles, you can create custom templates that suit your specific needs and use cases. The following code example shows how to customize the timeline cell tooltip in Gantt Chart.

```cshtml
@using Syncfusion.Blazor.Gantt

<SfGantt @ref="Gantt" DataSource="@TaskCollection" Height="450px" Width="1000px">
    <GanttTaskFields Id="TaskId" Name="TaskName" StartDate="StartDate" EndDate="EndDate" Duration="Duration"
                     Progress="Progress" ParentID="ParentId">
    </GanttTaskFields>
    <GanttTimelineSettings ShowTooltip="true"></GanttTimelineSettings>
    <GanttTooltipSettings TValue="TaskData">
       <TimelineCellTemplate> 
            @{ 
                var timelineCell = context as string; 
                <div>
                    <i class="app-icon-calendar"></i>
                    @timelineCell 
                </div>
         } 
        </TimelineCellTemplate>
    </GanttTooltipSettings>
</SfGantt>
@code {
    public SfGantt<TaskData> Gantt;
    public List<TaskData> TaskCollection { get; set; }
    private DateTime ProjectStartDate = new DateTime(2021, 04, 02);
    private DateTime ProjectEndDate = new DateTime(2022, 01, 01);
    protected override void OnInitialized()
    {
        this.TaskCollection = EditingData();
    }
    public class TaskData
    {
        public int TaskId { get; set; }
        public string TaskName { get; set; }
        public DateTime? StartDate { get; set; }
        public DateTime? EndDate { get; set; }
        public string Duration { get; set; }
        public int Progress { get; set; }
        public string Predecessor { get; set; }
        public string Notes { get; set; }
        public int? ParentId { get; set; }
    }
    public static List<TaskData> EditingData()
    {
        List<TaskData> Tasks = new List<TaskData>() {
        new TaskData() { TaskId = 1, TaskName = "Product concept", StartDate = new DateTime(2021, 04, 03), EndDate = new DateTime(2021, 04, 08), Duration = "5 days" },
        new TaskData() { TaskId = 2, TaskName = "Defining the product usage", StartDate = new DateTime(2021, 04, 01), EndDate = new DateTime(2021, 04, 08), Duration = "3", Progress = 30, ParentId = 1 },
        new TaskData() { TaskId = 3, TaskName = "Defining the target audience", StartDate = new DateTime(2021, 04, 02), EndDate = new DateTime(2021, 04, 04), Duration = "3", Progress = 40, ParentId = 2 },
        new TaskData() { TaskId = 4, TaskName = "Prepare product sketch and notes", StartDate = new DateTime(2021, 03, 28), EndDate = new DateTime(2021, 04, 08), Duration = "2", Progress = 30, ParentId = 3, Predecessor="2" },
        new TaskData() { TaskId = 5, TaskName = "Concept approval", StartDate = new DateTime(2021, 04, 08), EndDate = new DateTime(2021, 04, 08), Duration="0",Predecessor="3,4" },
        new TaskData() { TaskId = 6, TaskName = "Market research", StartDate = new DateTime(2021, 04, 09), EndDate = new DateTime(2021, 04, 18), Predecessor="2", Duration = "4", Progress = 30 },
        new TaskData() { TaskId = 7, TaskName = "Demand analysis", StartDate = new DateTime(2021, 04, 09), EndDate = new DateTime(2021, 04, 12), Duration = "4", Progress = 40, ParentId = 6 },
        new TaskData() { TaskId = 8, TaskName = "Customer strength", StartDate = new DateTime(2021, 04, 09), EndDate = new DateTime(2021, 04, 12), Duration = "4", Progress = 30, ParentId = 7, Predecessor="5" },
    };
        return Tasks;
    }
}
<style>
    @@font-face {
        font-family: 'Gantt control icon';
        src: url(data:application/x-font-ttf;charset=utf-8;base64,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) format('truetype');
        font-weight: normal;
        font-style: normal;
    }

    i {
        font-family: 'Gantt control icon' !important;
        speak: none;
        vertical-align: sub;
        font-size: 18px;
        font-style: normal;
        font-weight: normal;
        font-variant: normal;
        text-transform: none;
        line-height: 1;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

    .app-icon-calendar:before {
        content: "\e700";
        width: 40px;
        height: 40px;
    }
</style>
```

![Blazor Gantt Chart displays Manual Taskbar Tooltip](images/timeline-cell-tooltip.png)