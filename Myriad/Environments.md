# Environments
The environments screen provides detailed information about the selected environment. At the top it displays the status as well as the environments impact, ie how much use it is receiving. The `Myr` environment comes with Myriad by default and allows the user to test out functionality of Myriad without having any changes applied to a working environment.

<img src="Media/Environments.png">

---
## Events
The events are located on the left hand side of the environment screen. It is used to view and edit events that are in this environment. At the top of the events section the pending events are displayed, and below those are the past events. You can search past events using the search bar provided. If you have the permissions you can edit these events or add new ones. Click an event to [view it in detail](Events.md).

In the 'Pending' section you can finish an event preventing its status from impacting the status of the environment. In the 'Past Events' section you can start events and they will start affecting the status of the environment. Learn more about [events](Events.md).

---
## Applications
This section on the right hand side of the screen lists all the applications for this environment. You can view notes as well as view any links for the application. You can enable website status icons that indicate if the website is currently accessible. You can configure the environment to automatically change event statuses if a URL goes from accessible to inaccessible. This allows a history to build automatically, as well as change the status of the entire environment. To learn more visit [Applications](Applications.md).

### Edit Applications
By clicking the `Edit Applications` button located in the upper right-hand corner of the applications list, you can edit the applications set up to this environment. At the top above the list you can see the tools you can use. There is a `Create` button that lets you add a new application to this environment. The `Make Editable` button makes every field in the applications list editable. The `↓ CSV` button allows you to download the list of applications as a csv file. Conversely the `↑ CSV` button lets you upload applications using a local csv file. This makes it easy to create environments that contain the same applications as other environments. Lastly the search box lets you search the applications for the one specified.  

<img src="Media/Environments-Edit-Applications.png">


---
## Environment Details
The environment details section is located below the applications list. Here you can view details about the environment like the name, owners, tests cases, and general compute like the number of processors, ram, and disk storage.

<img src="Media/Environments-Details.png" width="400">
