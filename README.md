# Angular-Guide
---
##### Md. Shohanur Rahman
***

- Install NPM
- Create New Project : `ng new my_project`
- Run Project `npm start`
- Create component `ng g c myComponent`
- Create guard `ng g g auth`

#### Errors
-ng.ps1 cannot be loaded. The file ng.ps1 is not digitally signed. You cannot run this script on the current system.
<br/>
Open terminal and hit commands step by step:
<br/>
`set-ExecutionPolicy RemoteSigned -Scope CurrentUser`
<br>
`Get-ExecutionPolicy`
<br>
`Get-ExecutionPolicy -list`
