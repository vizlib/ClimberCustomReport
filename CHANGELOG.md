# cl-custom-report change log

All notable changes to this project will be documented in this file.

Project versioning adheres to [Semantic Versioning](http://semver.org/).
Commit convention is based on [Conventional Commits](http://conventionalcommits.org).
Change log format is based on [Keep a Changelog](http://keepachangelog.com/).

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


