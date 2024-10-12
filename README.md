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
export const authGuard: CanActivateFn = (route, state) => {
  const router = inject(Router);
  const token = localStorage.getItem("KPIMSWebApp");
  if(token != null)
    return true;

  router.navigateByUrl("account/login");
  return false;
};

```



- ###### Create interceptor (for passing bearer token): `ng g interceptor apiHelper`
```
export const apiHelperInterceptor: HttpInterceptorFn = (req, next) => {
  const token = localStorage.getItem("KPIMSWebApp");
  const request = req.clone({
    setHeaders: {
      Authorization: `Bearer ${token}`
    }
  });
  return next(request);
};

```

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
