---
title: set-up-automatic-snapshot-creation
displayName: Set up automatic snapshots
order: 20
published: true
toc:
   --1--Create a schedule: "create-a-schedule"
   --2--Create a schedule and give it a name: "create-a-schedule-and-give-it-a-name"
   --2--Select volumes: "select-volumes"
   --2--Add and configure a snapshot schedule for volumes: "add-and-configure-a-snapshot-schedule"
   --3--name template: "1-click--add-schedule--and-enter-a-name-for-future-snapshots"
   --3--max resource count: "2-set-the-maximum-resource-quantity"
   --3--schedule       type: "3-select-the-schedule-type----custom--or--period"
   --3--retention time: "4-set-the-snapshots-retention-time"
   --2--Add multiple snapshot schedules if needed: "add-multiple-snapshot-schedules-if-needed"
   --1--How to disable and enable a schedule: "how-to-disable-and-enable-a-schedule"
   --1--How to delete a schedule: "how-to-delete-a-schedule"
---
# Set up automatic snapshot creation

Snapshot Schedules is a feature that allows you to automate the creation of snapshots for your volumes based on your preferred day, hour, and minute, or at regular intervals. Moreover, it can automatically update your snapshots, such as creating a new one and deleting the previous one every day.

You can access this feature by logging into your personal account and navigating to the Snapshot Schedules section within your project. We'll provide you with instructions on how to use this feature.

<img src="https://support.gcore.com/hc/article_attachments/5286498706961/mceclip0.png" alt="mceclip0.png">


## Create a schedule

### Create a schedule and give it a name

Open “Snapshot Schedules” and click “Create Snapshot Schedule” in the upper right corner. The system will ask you to enter a name. Name the schedule so that it will be easier to distinguish it from others later — for example, you can use a volume name: "Snapshot of \[your volume name\]".

[<img src="https://support.gcore.com/hc/article_attachments/5286531058321/mceclip0.png" alt="mceclip0.png"><img src="https://support.gcore.com/hc/article_attachments/5286548993297/mceclip1.png" alt="mceclip1.png">](https://support.gcorelabs.com/hc/article_attachments/360019886678/mceclip1.png)

Click on the created schedule to configure it.

<img src="https://support.gcore.com/hc/article_attachments/5286592054929/mceclip2.png" alt="mceclip2.png">

### Select volumes

Click "Add Volume" at the bottom of the page. Select one or several volumes for which snapshots will be created; you can choose both boot and regular volumes.

[<img src="https://support.gcore.com/hc/article_attachments/360019793517/mceclip11.png" alt="mceclip11.png" width="322" height="389">](https://support.gcorelabs.com/hc/article_attachments/360019793517/mceclip11.png)    [<img src="https://support.gcore.com/hc/article_attachments/360019893418/mceclip41.png" alt="mceclip41.png" width="361" height="389">](https://support.gcorelabs.com/hc/article_attachments/360019893418/mceclip41.png)

Confirm your choice by clicking "Save" in the pop-up window.

[<img src="https://support.gcore.com/hc/article_attachments/360019893438/mceclip42.png" alt="mceclip42.png" width="306" height="142">](https://support.gcorelabs.com/hc/article_attachments/360019893438/mceclip42.png)

### Add and configure a snapshot schedule

1. Click "Add Schedule" and enter a name for future snapshots

   [<img src="https://support.gcore.com/hc/article_attachments/360019893558/mceclip43.png" alt="mceclip43.png" width="311" height="378">](https://support.gcorelabs.com/hc/article_attachments/360019893558/mceclip43.png)   [<img src="https://support.gcore.com/hc/article_attachments/360019794117/mceclip18.png" alt="mceclip18.png" width="343" height="377">](https://support.gcorelabs.com/hc/article_attachments/360019794117/mceclip18.png)

In the "Name template" field, enter a name for future snapshots. All Snapshots created within this schedule will receive it. You can use the dynamic variable "{volume\_id}" in the template — it will be replaced with your volume's name automatically. For example, if the volume is named "Disk\_1" and the Name template is "Snapshot of {volume\_id}", then the system will create the snapshot “Snapshot of Disk\_1”.

2. Set the maximum resource quantity

[<img src="https://support.gcore.com/hc/article_attachments/360019890258/mceclip20.png" alt="mceclip20.png" width="322" height="356">](https://support.gcorelabs.com/hc/article_attachments/360019890258/mceclip20.png)

“Max resource count” limits the number of snapshots within the schedule. If the limit is reached, the system will delete the old one to free up space before creating a new Snapshot.

Example. You have configured a schedule that creates a snapshot every day and its maximum number of resources is 5. You launched it on Monday. By the end of Friday, the system has already made 5 snapshots. It will free up space on Saturday by deleting the oldest snapshot (Monday’s) and create a new one. The same will be done on Sunday and all subsequent days. Snapshots created within another schedule or manually will not be affected by the system.

3. Select the schedule type — "Custom" or "Period"

[_<img src="https://support.gcore.com/hc/article_attachments/360019795037/mceclip23.png" alt="mceclip23.png" width="320" height="321">_](https://support.gcorelabs.com/hc/article_attachments/360019795037/mceclip23.png)

_With the “Custom” schedule,_ you can specify months, days of week, hours and minutes for creation of snapshots. For example, if you select the months January and May, the day Monday and the time 16:00, the system will create about 8 snapshots per year — at 16:00 every Monday in January and May.

When choosing your time zone, notice that Etc/GMT and GMT are not the same things. Etc/GMT values ​​are opposite to GMT — for example, London time can be specified as Etc/GMT-1 or GMT+1.

[<img src="https://support.gcore.com/hc/article_attachments/360019891258/mceclip24.png" alt="mceclip24.png" width="349" height="328">](https://support.gcorelabs.com/hc/article_attachments/360019891258/mceclip24.png)

_With the "Period" schedule type,_ you specify the regular intervals at which the system should take a snapshot. The minimum interval is 1 hour. For example, you can set up a period of 1 week and get a snapshot every seven days. After starting the schedule, the system will wait until the required period has passed and take a snapshot. When the period passes again, it will do the second one, and so on.

4. Set the snapshots retention time

[<img src="https://support.gcore.com/hc/article_attachments/360019891538/mceclip26.png" alt="mceclip26.png" width="419" height="127">](https://support.gcorelabs.com/hc/article_attachments/360019891538/mceclip26.png)

Define the retention time — the period after which the snapshot will be automatically deleted. For example, if a snapshot is created on Monday with the retention time of 2 days, the system will delete it on Wednesday.

Please note: even if the retention time has not expired, the system may delete an old snapshot if there is no space for a new one. This process depends on the maximum resource quantity. If you specified the maximum resource quantity of 5 and the system has to take the 6th Snapshot, before that it will delete the oldest one (1st), even if its retention time has not expired.

5. Save the schedule.

[<img src="https://support.gcore.com/hc/article_attachments/360019891758/mceclip27.png" alt="mceclip27.png" width="343" height="415">](https://support.gcorelabs.com/hc/article_attachments/360019891758/mceclip27.png)

When all the settings are configured, click "Save" —  the schedule will start and the system will start taking snapshots.

Add multiple snapshot schedules if needed

You can create multiple schedules for the selected volumes — for example, if you want to receive a snapshot every Monday at 15:22 and every Saturday at 19:00, add a separate Custom schedule for each of them.

[<img src="https://support.gcore.com/hc/article_attachments/360019892058/mceclip30.png" alt="mceclip30.png" width="415" height="169">](https://support.gcorelabs.com/hc/article_attachments/360019892058/mceclip30.png)

## How to disable and enable a schedule

Once created, each schedule is enabled by default and starts running. It gets the status "Active".

[<img src="https://support.gcore.com/hc/article_attachments/360019892438/mceclip38.png" alt="mceclip38.png" width="670" height="110">](https://support.gcorelabs.com/hc/article_attachments/360019892438/mceclip38.png)

To disable a schedule, open it and drag the slider at the top of the screen to the right. Then click "Save" You can later enable the schedule again using this slider.

  [<img src="https://support.gcore.com/hc/article_attachments/360019796257/mceclip39.png" alt="mceclip39.png" width="311" height="386">](https://support.gcorelabs.com/hc/article_attachments/360019796257/mceclip39.png)  [<img src="https://support.gcore.com/hc/article_attachments/360019909878/mceclip0.png" alt="mceclip0.png" width="318" height="386">](https://support.gcorelabs.com/hc/article_attachments/360019909878/mceclip0.png)

You cannot disable and edit a separate schedule of the “Custom” or “Period” type, but you can delete it. To do this, open the schedule and click "Delete".

[<img src="https://support.gcore.com/hc/article_attachments/360019893738/mceclip44.png" alt="mceclip44.png" width="332" height="136">](https://support.gcorelabs.com/hc/article_attachments/360019893738/mceclip44.png)  
[<img src="https://support.gcore.com/hc/article_attachments/360019797677/mceclip45.png" alt="mceclip45.png" width="333" height="460">](https://support.gcorelabs.com/hc/article_attachments/360019797677/mceclip45.png)

## How to delete a schedule

You can delete the entire schedule in the “Snapshot Schedules” section. To do this, click on the ellipsis near the required schedule and select "Delete" in the drop-down menu.

<img src="https://support.gcore.com/hc/article_attachments/5286607320977/mceclip3.png" alt="mceclip3.png">