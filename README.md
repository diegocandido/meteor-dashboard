Based of current Version: ``July 10, 2015``

## Meteor Implementation of Pages Theme
This Project currently includes following components.

##### Dashboard
 - [ ] ToDo: still depends on JSON Data
 - [ ] ToDo: mapplic map has wrong resource path

##### Portlets
##### UI Elements
 - [ ] ToDo: Icons -> Line Icons missing

##### Forms
 - [ ] ToDo: add Wizard

##### Tables

##### Charts
 - **Important**: [Rickshaw Graphing Library can not be minified by meteors](https://github.com/meteor/meteor/issues/1360) uglifier because the `$super` variable needs to persist. It needs to be loaded on-side via `$.getScript()` or similar.

##### Extras
- Blank
- Login
  - [ ] ToDo: Navigating from inside the app via link to the `/login` breaks layout due to no proper de-initialisation of sidebar / pages code. Directly navigating to /login works fine.

## Tech Spec
 * Layout uses FlowRouter
  * iron:router was switched out due to recent trouble in the community / no continuation
 * Begun, where easily possible, to scope jQuery actions `$` to the template `tpl.$`
  * has the benefit to freely re-use templates without css-properties/classes (ie. widget-1320)
    - [ ] ToDo: not all methods are scoped to template specifics. Danger of beyond component dom-manipulations.
 * Some code clean-up and consistency in naming conventions. Semicolons for magnifications etc. mostly according to [meteor style guide](https://github.com/meteor/meteor/wiki/Meteor-Style-Guide)
