# Angular-Guide
---
##### Md. Shohanur Rahman
***

- ###### Install NPM
- ###### Create New Project : `ng new my_project`
- ###### Run Project: `npm start`
- ###### Create component: `ng g c myComponent`
###### How to create angular guard: 
- run command `ng g g auth`
- after that add bellow code to guard
```
function test() {
  console.log("notice the blank line before this function?");
}
```



- ###### Create interceptor (for passing bearer token): `ng g interceptor apiHelper`

#### Errors
- #### ng.ps1 cannot be loaded. The file ng.ps1 is not digitally signed. You cannot run this script on the current system.
<br/>
Open terminal and hit commands step by step:
<br/>
`set-ExecutionPolicy RemoteSigned -Scope CurrentUser`
<br>
`Get-ExecutionPolicy`
<br>
`Get-ExecutionPolicy -list`
