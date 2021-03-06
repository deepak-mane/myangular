# Angular | app-routing.module.ts

- Entire sample angular project uploaded under [here](./sample_prj/routing-start.zip)

```typescript
import { NgModule } from "@angular/core";
import { Routes, RouterModule } from "@angular/router";

import { HomeComponent } from "./home/home.component";
import { UsersComponent } from "./users/users.component";
import { UserComponent } from "./users/user/user.component";
import { ServersComponent } from "./servers/servers.component";
import { ServerComponent } from "./servers/server/server.component";
import { EditServerComponent } from "./servers/edit-server/edit-server.component";
import { PageNotFoundComponent } from "./page-not-found/page-not-found.component";
import { AuthGaurd } from "./auth-gaurd.service";


const appRoutes: Routes = [
    { path: '' ,component: HomeComponent ,pathMatch: 'full'},
    { path: 'users' ,component: UsersComponent, children: [
        { path: ':id/:name' ,component: UserComponent },
      ] 
    },
    { path: 'servers' , 
      // canActivate: [AuthGaurd],
      canActivateChild: [AuthGaurd],
      component: ServersComponent, 
      children: [
        { path: ':id' ,component: ServerComponent },
        { path: ':id/edit' ,component: EditServerComponent },
      ] 
    },
    { path: 'not-found', component: PageNotFoundComponent},
    { path: '**', redirectTo: '/not-found'}
  ];
  
  

@NgModule({
   imports: [
       RouterModule.forRoot(appRoutes)
   ], 
    exports: [
        RouterModule
    ]
})

export class AppRoutingModule {

}
```
