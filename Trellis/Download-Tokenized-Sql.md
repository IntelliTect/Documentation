# Download Tokenized SQL for a Snapshot or Change package
Sometimes a database is needed in multiple environments. But what if the database contains environment-specific data that would require a different copy for each environment? Thats where Trellis comes in. You can store the environment-specific data in tokens that are replaced by variables. That means changes to these variables will not be detected as changes. Generally this is not used frequently.

* Start by creating or viewing [a Comparison](Snapshot-Comparisons.md) or [Change Package](Change-Packages.md)
* From the change package overview screen select the "Download Tokenized SQL" button in the upper righthand corner of the header
* Select the location to save
* Trellis will insert SQL variable into the columns specified, and declare the sql variables at the top of the downloaded SQL.