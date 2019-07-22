---
title: "Event APIs"
sidebar: myriad_sidebar
permalink: docs/Myriad/Event-APIs.html
---

 
# Event APIs 
Myriad supports an API to update events. This can be used to tie in other applications or for updating event status from a build script or other automated tooling. The `Help` button at the top will display the application documentation. Selecting the `API Docs` button will then show detailed information and examples. 
 
For example, a build script for a lower environment might automatically: 
 
* Create an event 
* Start the event 
* Provide a status update 
* Associate work items 
* Finish the event 
* This causes email alerts to be sent to the subscribed users automatically, eliminating the need for manual emails. 
 
--- 
## Accessing the API 
By making a POST to the URL `https://myriad.corp.com/api/event/AddUpdate` you can add, create, and edit events. There is a PowerShell module that allows users to perform these operations directly from the command line. The module can be downloaded from [here](http://localhost:30648/Help/DownloadPSScript). 
 
--- 
## Example PowerShell Command 
Creates and starts a new event for a CCB deployment to MOD with 3 work items: 
* `$event = Push-MyriadEvent -Environment MOD -EventType Deployment -Application 'CC&B' -AssignedTo 'Heidi Smith' -Impact Medium -Status Start -WorkItemIds ('D-03800', 'D-03646', 'D-03847') -ScheduledEnd ([DateTime]::Now.AddHours(1))` 
 
Adds a status note to the event that was just created: 
* `Push-MyriadEvent -EventId $event.eventId -Note "Work Continues"` 
 
An alternate way to add a status without access to the Event's ID: 
* `Push-MyriadEvent -Environment MOD -EventType Deployment -Application 'CC&B' -Note "Work Continues"` 
 
Finishes the event: 
* `Push-MyriadEvent -EventId $event.eventId -Status Finish` 
 
An alternate way to finish the same event without access to the Event's ID: 
* `Push-MyriadEvent -Environment MOD -EventType Deployment -Application 'CC&B' -Status Finish` 

