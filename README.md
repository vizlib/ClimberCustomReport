# Climber Custom Report
<a href="http://www.climberextensions.com/" class="image_link"  target="_blank"><img src="./screenshots/downloadbutton.png?raw=true" 
alt="Download latest release" width="400" height="40" border="0" /></a>  

## Most recent update 2.6.1 - 2019-03-11
### Fixed
- ES-11497 Alert variable already exists

Full CHANGELOG can be found end of this file.

<div style="page-break-after: always;"></div> 

 ### Self service without edit-mode for Qlik Sense!  

<img src="./screenshots/CustomReport.gif?raw=true" alt="Custom Report" />

## Purpose and Description
**IMPORTANT! Any older Custom Report objects need to be recreated with version 2.0!**

In QlikView we saw a lot of users requesting a customizable straight table. In Qlik Sense we have created something even better! The Custom Report extension allows the user to create custom tables based on data in master tables. 

With Custom Report + you can create your own personalized bookmarks and add shareable presets for your reports. In Custom Report + we have also extended the visualization types to include pivot tables and combo charts (more details below). 

First thing to do is create a simple straight table and make it a master item. The table is will now be accessible in Custom Report and you can select to show any or all measures and dimensions. Number format follows from the master item so no need to redo formatting! 

**Tested with Qlik Sense November 2017 and later**

<div style="page-break-after: always;"></div> 

## Custom Report vs Custom Report +

<img src="./screenshots/CustomReport+.png?raw=true" alt="CustomReport+"/>

For more information about Custom Report + and our subscription model please check out our extension <a href="https://www.climberextensions.com"> page </a>.

## Setup

1. Create one or more Master Item Tables with the dimensions and measures you want to visualize.   
  
2. Select Master Item in the drop-down or drag and drop it on the visualization

<img src="./screenshots/AddnewDataSet.gif?raw=true" alt="Add new Data Set to Custom Report" />

## Defaults, presets and bookmarks

### Default states

All added data sets can have a default state when a new session is opened, i.e. preselected dimensions and measures. Even the table column widths are saved in the state. It is recommended to always set a default state so the user does not have to start with an empty table.

To create a new default state for a dataset go in to edit mode. Select your measures/dimensions you want to set in you default state and click "Save default state". After you added a default state you can always show your current default state by clicking on the button "show default state". 

To change your default state, just make your new selections and click "Save default state" again.

-Save default state
<img src="./screenshots/DefaultState.png?raw=true" alt="Default State" /> 

-Show default state
<img src="./screenshots/ShowDefaultState.png?raw=true" alt="Show Default State" />   

### Session

Within a session, all selections between the data sets will be saved, i.e. the default state will not be followed once the session is started. This makes it possible to easily change between data sets without losing the last state.

<div style="page-break-after: always;"></div> 

### Presets (Custom Report+)

It is possible for the developer/super users to create presets (i.e. a saved state). Presets will be accessible for all users in the application. This can be used for creating predefined reports.

Presets are accessible from the drop down of data sets 

<img src="./screenshots/Presets.png?raw=true" alt="Presets" /> 

To create a preset select your dimensions/measures and go in to edit mode. Click on "presets" and click on "Add Preset". To change a preset, change your selections and click "Save preset". 

You can always show a current preset by clicking "show preset" 

<img src="./screenshots/PresetsCreate.png?raw=true" alt="PresetsCreate" />

<div style="page-break-after: always;"></div> 

### Bookmarks (Custom Report+)
For the end user is possible to create personalized bookmarks. With bookmarks you can save a state and go back to that state using the standard Qlik Sense bookmark list. 

How to use bookmarks

1. Enable bookmarks in Custom Report Object (enabled is default)

<img src="./screenshots/EnableBookmarks.png?raw=true" alt="Enable Bookmarks" />

2. Use the bookmark creator <a href="https://help.qlik.com/en-US/sense/2.1/Subsystems/Hub/Content/Bookmarks/create-bookmark.htm"> How to create a bookmark </a>

<img src="./screenshots/CreateBookmarks.png?raw=true" alt="Create Bookmark" />

3. Access the bookmarks 

<img src="./screenshots/AccessBookmarks.png?raw=true" alt="Access Bookmark" />

*Note!* To support bookmarks using the Qlik Sense standard functionality, the extension creates and use variables starting with "ClimberCustomReport". These variables values are stored in the selection state and therefore in bookmarks. This is not the default behaviour of variables created in the Qlik Sense client. If you accidently delete the variable, entering Edit mode will recreate it if the app is not published. Variables are not automatically deleted. In the Custom Report+ state is stored even if Use Bookmarks is not enabled, but only applied if enabled.  
*Note!* If the Custom Report should be used as a master items it need to disable Use Bookmarks and then enabled, after it's been added to the master library. This is due to the Custom Reports gets a new Id and a new variable needs to be created.  

<div style="page-break-after: always;"></div> 

## Sort Bar

With the sort bar you can change the order of the dimensions and measures. It is possible to hide the sort bar for different visualizations types. 

*From QS February 2018 it's possible to change column order in a table by dragging in the column header so typically a straight table does not need the Sort Bar*

<img src="./screenshots/SortBar.gif?raw=true" alt="SortBar" />

<img src="./screenshots/HideTheSortBar.png?raw=true" alt="Hide the SortBar" />

<div style="page-break-after: always;"></div> 

## Other options

1. The objects used are standard Qlik Sense objects so all standard features such as export and sorting are available (Export to image/pdf does not work. See limitations below.)

2. Using a minimized version of the object you can put a custom report on any sheet along with the rest of the visualizations. Click arrows to expand to full screen!  

3. Right-click menu allows you to make changes even with fields/sortbar hidden  

4. Search in dimensions and measure list

5. Clear all selections

6. Add totals to table/pivot table
<img src="./screenshots/AddTotals.png?raw=true" alt="AddTotals" />

7. Right-click selected dimension/measures. Dimensions only for Pivot Table, both for Combo chart. Table handle sort inside the visualization.  
<img src="./screenshots/SortDimensionMeasure.png?raw=true" alt="Sort Dimension/Measure" />  

<div style="page-break-after: always;"></div> 

## Copy value Ctrl + C
Copy the value under the mouse cursor by pressing Ctrl + C. A notification will confirm the copied value at the bottom of the screen.
<img src="./screenshots/copy-value-to-clipboard.png?raw=true" alt="Copy value notification" />  

## Copy table Shift + C (Custom Report+)
Copy the data table of the current visualization of it is less than 10 000 cells. A notification will appear at the bottom of the screen when the data is exported. Click the toast "Copy table to clipboard" to copy the table.

<img src="./screenshots/copy-table-to-clipboard.png?raw=true" alt="Copy table notification" />  

<div style="page-break-after: always;"></div> 

## Export to new application

It is possible to export the current state of a selected data set to a new application. In the new application, master items will be created from your dimension and measures. In Qlik Sense Enterprise the user need to have security rights to create an app for the feature to work. For June 2018 and later releases the new app will open in "Generate Insights"-mode that suggest charts based on the data. 

<img src="./screenshots/ExporttonewApp.gif?raw=true" alt="ExporttonewApp" />

## Export to new application using a template (Custom Report+)

To enable this feature, Enable export to template features in the experimental settings (Settings\Experimental Settings). 

<div style="page-break-after: always;"></div> 

## Installation

1. Download the latest version of Qlik Sense (QS November 2017 or higher)
2. Qlik Sense Desktop
    * To install, copy all files in the .zip file to folder "C:\Users\\[%Username%]\Documents\Qlik\Sense\Extensions\cl-customreport\"
3. Qlik Sense Server
    * See instructions <a href="http://help.qlik.com/en-US/sense/Subsystems/ManagementConsole/Content/import-extensions.htm"> how to import an extension on Qlik Sense Server </a>

## Limitations

* Calculation conditions in master items are not respected
* Master measure/dimension colors only in Combo chart
* A very small (collapsed) version of the extension could look nicer :-)
* Export to template only works in Qlik Sense Enterprise
* Unpublished sheets in a published app can't use Bookmarks
* Expression labels doesn't work in Qlik Sense November 2017 or prior
* Expression labels only work for master measures/dimensions
* Step back/forward needs to be clicked twice if a measure/dimension is added/removed (only Custom Report+)
* Export to image/pdf in QAP only exports the table/pivot/combo visualization
* Export to image/pdf, when used in a Climber Container+, only exports the table/pivot/combo visualization

## Recommended Versions
Qlik Sense Version | Recommended
------------- | -------------
February 2018|*2.6.1*
November 2018|*2.6.1*
September 2018|*2.6.1*
June 2018|*2.6.1*
April 2018|*2.6.1*
February 2018|*2.6.1*
November 2017|*2.6.1*
September 2017|*2.6.1*


<div style="page-break-after: always;"></div>  

## Climber Extensions
Like this extension? Check out the other Climber extensions below or visit <a href="http://www.climberextensions.com"> climberextensions.com </a> for more information about our extensions offerings.

**Finance Report (P&L)**
* https://www.youtube.com/watch?v=xOfShi94T4k
(No free version available, only on subscription.)

**Container**
* https://github.com/ClimberAB/ClimberContainer

**Selection Bar**
* https://github.com/ClimberAB/ClimberSelectionBar
* https://www.youtube.com/watch?v=4fxrphADRKw

**KPI**
* https://github.com/ClimberAB/ClimberKPI
* https://www.youtube.com/watch?v=9zdfYshNel4

**Cards**
* https://github.com/ClimberAB/ClimberCards
* https://www.youtube.com/watch?v=k_IEt8TvB_c

**Climber**
* http://github.com/ClimberAB

## Change Log
## 2.6.1 - 2019-03-11 
### Fixed
- ES-11497 Alert variable already exists 
 
## 2.6.0 - 2019-02-21 
### Added
- Support for February 2019
- Copy cell to clipboard
- QAP export to image/pdf
### Added (Plus-version)
- Copy table to clipboard
- Added dimensions are added as rows
- Override for Include null values in Pivot table
### Fixed
- ES-10058 Defered state reverts when sorting
- ES-9963 Show Details expanded / Hide fields/Sort bar doesn't persist
- Column widths not persisted in state 
 
## 2.5.0 - 2018-12-03 
### Added
- Support for November 2018
- Bundle information
### Added (Plus-version)
- Export to image/pdf/ppt
- Snapshot
### Fixed
- ES-10495 & ES-10494 Combochart state undefined
- Alternative state tab in property panel November 2018 and later
### Removed (Free-version)
- Export data 
 
## 2.4.4 - 2018-10-28 
### Fixed 
- Export data 'Invalid parameter' issue September 2017
- License for plus and normal versions. 
 
## 2.4.3 - 2018-09-29 
### Fixed 
- Added Code Change Warning
- Fixed #74 Climber Icon 
 
## 2.4.2 - 2018-09-20 
### Fixed (Plus-version)
- Add lint to CircleCi
- Possible fix ES-9371
- Fixed ES-9905 Master Item description on title hoover
- Fixed ES-9720 export from Mashup proxy prefix replace
- Fixed IE export and render problem 
 
## 2.4.1 - 2018-09-06 
### Fixed (Plus-version)
- Fixed ES-9720 Combo chart doesn't render if previous state exist 
 
## 2.4.0 - 2018-08-30 
### Added
- Show details
- Hide data sets
- Hide visualization settings
- Hide export to app
- Hide export data
- Hide visibility fields and sortbar
- Hide switch data sets 
- Hide add/remove items
- Icons option for changing visualization types
### Added (Plus-version)
- Show data labels Combo chart
- Show data points Combo chart
- Sort dimensions/measures Combo chart
- Sort dimensions Pivot table
### Changed
- Totals on as default
- Reorganized settings in property panel
### Fixed
- Perfect scrollbar bug
- Fixed Export to app, fields with dangling spaces. 
 
## 2.3.0 - 2018-08-02 
### Added (Plus-version)
- Defer layout update (experimental feature)
### Changed
- Climber Custom Report and Custom Report+ releases are from now on synced
- Disable Use expression labels in QS Nov 2017 and prior
### Fixed
- Selections drop with large apps
- qColumnOrder property sync issue
- Reflow issue and CSS improvements (Firefox)
### Fixed (Plus-version)
- Step back/forward issue 
 
## 2.2.1 - 2018-07-18 
### Fixed
- Source on Github out of sync with release 
 
## 2.2.0 - 2018-07-18 
### Fixed
- Issues introduced with 2.1.2 and 2.1.3 
 
## 2.1.3 - 2018-07-13 
### Fixed
- Fixed parameters for pivot table and combochart for before april 2018 versions. (Plus-version)
- Corrected timeout parameter.
- Fixed expression labels don't show as default when upgrading from 1.3.x to 2.x, even though property is set to false. 
 
## 2.1.2 - 2018-07-11 
### Fixed
- Fixed patch timeout for dimension och measure selections.
- Hotfix for export url in mashup environments. 
 
## 2.1.1 - 2018-06-29 
### Fixed
- Fixed swaping columns
- Fixed Export title name 
 
## 2.1.0 - 2018-06-21 
### Added
- Use expression labels option
- Option to sort selected items first, default value true
- Context menu include zero values  
- Custom Export data dialog, that works in a mashup 
### Changed
- Export to new app goes to insights mode if June 2018 or later
- Improved error message on export to app
### Fixed
- Export to new app/template for values sometimes is exported as NaN
- Export to new app/template dual fields with spaces
- Works with QS June 2018
- Fix selections after search
- Improved clean up.
- Overflow caused by textarea 
 
## 2.0.3 - 2018-05-24 
### Fixed
- Can be used in a Container extension like Climber Container. 
 
## 2.0.2 - 2018-05-07 
### Changed
- Sums on/off
- Search dimensions/measures
- Clear all dimensions/measures
- Export to app
- Hide/Show sort bar
- Respect zero value settings in master table
- One default state per data set (previously one per custom report object)
- Remember column width within a session
- Updated license 
 
## 2.6.1 - 2019-03-11 
### Fixed
- ES-11497 Alert variable already exists 
 
## 2.6.0 - 2019-02-21 
### Added
- Support for February 2019
- Copy cell to clipboard
- QAP export to image/pdf
### Added (Plus-version)
- Copy table to clipboard
- Added dimensions are added as rows
- Override for Include null values in Pivot table
### Fixed
- ES-10058 Defered state reverts when sorting
- ES-9963 Show Details expanded / Hide fields/Sort bar doesn't persist
- Column widths not persisted in state 
 
## 2.5.0 - 2018-12-03 
### Added
- Support for November 2018
- Bundle information
### Added (Plus-version)
- Export to image/pdf/ppt
- Snapshot
### Fixed
- ES-10495 & ES-10494 Combochart state undefined
- Alternative state tab in property panel November 2018 and later
### Removed (Free-version)
- Export data 
 
## 2.4.4 - 2018-10-28 
### Fixed 
- Export data 'Invalid parameter' issue September 2017
- License for plus and normal versions. 
 
## 2.4.3 - 2018-09-29 
### Fixed 
- Added Code Change Warning
- Fixed #74 Climber Icon 
 
## 2.4.2 - 2018-09-20 
### Fixed (Plus-version)
- Add lint to CircleCi
- Possible fix ES-9371
- Fixed ES-9905 Master Item description on title hoover
- Fixed ES-9720 export from Mashup proxy prefix replace
- Fixed IE export and render problem 
 
## 2.4.1 - 2018-09-06 
### Fixed (Plus-version)
- Fixed ES-9720 Combo chart doesn't render if previous state exist 
 
## 2.4.0 - 2018-08-30 
### Added
- Show details
- Hide data sets
- Hide visualization settings
- Hide export to app
- Hide export data
- Hide visibility fields and sortbar
- Hide switch data sets 
- Hide add/remove items
- Icons option for changing visualization types
### Added (Plus-version)
- Show data labels Combo chart
- Show data points Combo chart
- Sort dimensions/measures Combo chart
- Sort dimensions Pivot table
### Changed
- Totals on as default
- Reorganized settings in property panel
### Fixed
- Perfect scrollbar bug
- Fixed Export to app, fields with dangling spaces. 
 
## 2.3.0 - 2018-08-02 
### Added (Plus-version)
- Defer layout update (experimental feature)
### Changed
- Climber Custom Report and Custom Report+ releases are from now on synced
- Disable Use expression labels in QS Nov 2017 and prior
### Fixed
- Selections drop with large apps
- qColumnOrder property sync issue
- Reflow issue and CSS improvements (Firefox)
### Fixed (Plus-version)
- Step back/forward issue 
 
## 2.2.1 - 2018-07-18 
### Fixed
- Source on Github out of sync with release 
 
## 2.2.0 - 2018-07-18 
### Fixed
- Issues introduced with 2.1.2 and 2.1.3 
 
## 2.1.3 - 2018-07-13 
### Fixed
- Fixed parameters for pivot table and combochart for before april 2018 versions. (Plus-version)
- Corrected timeout parameter.
- Fixed expression labels don't show as default when upgrading from 1.3.x to 2.x, even though property is set to false. 
 
## 2.1.2 - 2018-07-11 
### Fixed
- Fixed patch timeout for dimension och measure selections.
- Hotfix for export url in mashup environments. 
 
## 2.1.1 - 2018-06-29 
### Fixed
- Fixed swaping columns
- Fixed Export title name 
 
## 2.1.0 - 2018-06-21 
### Added
- Use expression labels option
- Option to sort selected items first, default value true
- Context menu include zero values  
- Custom Export data dialog, that works in a mashup 
### Changed
- Export to new app goes to insights mode if June 2018 or later
- Improved error message on export to app
### Fixed
- Export to new app/template for values sometimes is exported as NaN
- Export to new app/template dual fields with spaces
- Works with QS June 2018
- Fix selections after search
- Improved clean up.
- Overflow caused by textarea 
 
## 2.0.3 - 2018-05-24 
### Fixed
- Can be used in a Container extension like Climber Container. 
 
## 2.0.2 - 2018-05-07 
### Changed
- Sums on/off
- Search dimensions/measures
- Clear all dimensions/measures
- Export to app
- Hide/Show sort bar
- Respect zero value settings in master table
- One default state per data set (previously one per custom report object)
- Remember column width within a session
- Updated license 
 


## License

See <a href="License.pdf"> LICENSE </a>


