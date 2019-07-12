# Events
Myriad has events... TODO

## Viewing Events
To view an event simply click it from the location you see it. Here is where you can configure events. 
<img src="Media/Events-View.png" width="400">

---
## Details
In the top left of the event screen you can see details about the event. Here you can view any of the high level details about the event including the status, status notes, the schedule and any systems that are impacted by this event.

There is also buttons that allow the user to [edit the event](#Editing-Events), add status notes, or open the chat. If an event is not currently running, you can start the event. This will star

---
## Editing Events
To edit an event from the event detail screen simply click the `Ddit` button. Here is where most of the configurable event is configured.
Administrator users can open additional options at the top. The title or description can be either set or changed. The event phase can be set but is for nothing more that clarity. Impact can be changed. The user assigned to the event. The scheduled start and end. 

If the event is running, you can set up auto notification here, or mute the currently set up events. The impacted applications can be set so it is clear what is being effected by this event. Any work items can be added from this menu. Events can be cancelled, cloned, saved or closed in this section.

<img src="Media/Events-Edit.png" width="400">

### Adding Work Items
Myriad has an integration with Microsoft Azure Devops that allows you to add work items from Devops to events. To add new work items you first must go to the edit event screen. From here there is an `Add Work Items Button` that opens the work item section. 

This is a simple area that lets you add work items by the Azure Id. You can select either CC&B or MAX system to add the item to. Multiple work items can be added at once by entering them as a comma separated list. Any existing work items show up here and can be removed easily. The state is usually set to "Added" but sometimes it may be useful to remove a work item from the environment by having an event.

<img src="Media/Events-Add-Work-Items.png" width="400">

---
## Event Planning and Tasks
Tasks are set up similarly to other planning softwares. If you are familiar with Gantt charts, this section is very similar except it is rotated 90 degrees. The main idea is that it runs top to bottom. Anything that is stacked makes the lower item a dependant of the upper one. If there are tasks in a row it means they can be ran concurrently and have no dependents. 

In the example below under "Turn Off Systems" there are several tasks in the same row, and there is one below them. That means the "Turn off CC&B", and "Show Maint.Page" tasks can run at the same time while the "Install Software" task must wait for those two to be completed before starting.

<img src="Media/Event-Tasks.png">
