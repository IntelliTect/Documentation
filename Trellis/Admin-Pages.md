# Admin Pages
The admin pages are used to view and configure the support data for Trellis. Here you can add users, assign roles, create databases, define schemas and much more.

## Admin page 
To open the admin page click the `Admin Pages` button from the upper righthand corner of the applications page.
You are greeted with a list of options each of which has a Table and Cards column. Table is used to configure Trellis for use on a desktop, and Cards are used to configure Trellis for use on a mobile device.
 <img src="Media/Admin-Page-Overview.png">

---
# Setting up a Database
To set up snapshotting of a database you must first have an Application Type and a Schema. Select the Database option from the Admin Page. 
* Here is where you setup basic database information like the name and connection string. 
* The read only username and password are used as authentication to connect to the database.  
* At the bottom you can take a snapshot immediately, schedule recurring snapshots, or test the database connection.

 <img src="Media/Setup-A-Database.png">

 ## Recurring Snapshots
 Recurring snapshots are used to automatically take a snapshot of a database daily. To schedule recurring snapshots,navigate to the bottom of the database admin page and select `Schedule Recurring Snapshots` and you will be prompted for whats called a "Cron String". 
 * The format of the Cron String is always `0 <minute> <hour> * *` where hour and minute make up the daily time to take the snapshot. Eg `0 30 11 * *` would setup the snapshot to be taken at 11:30 every day. 
 * Its a good idea to check the [Hangfire](#Hangfire) page to ensure the recurring snapshot is setup. 
  

# Schema Table Selector
The Trellis schema table selector allows you to configure which tables in a database are enabled for snapshotting.

* To use the Schema Table Selector you first need to have a [Database](#Create-a-Database).
* Then you can select the Schema Table Selector option on the right hand side of the screen. 
* You are prompted to select a schema for a particular Application Type.
  
 <img src="Media/Schema-Table-Selector-Schema-Select.png">

Next select a database from the dropdown. A list of tables in the selected database will appear. You can enable or disable these tables. If a table is enabled, it will be used in both automatic and manually taken snapshots.
 <img src="Media/Schema-Table-Selector-Enabling.png">

# Hangfire
Hangfire is used to run the underlying Trellis jobs. You can use this screen to view all jobs, recurring jobs, and and jobs that have failed. It is accessed from the `Hangfire` link on the admin page. 

 <img src="Media/Hangfire.png">
