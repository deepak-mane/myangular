# myangular
Learnings of Angular,NodeJS,JavaScript

```typescript
npm install --save-dev @angular-devkit/build-angular
npm install -g @angular/cli
npm install bootstrap@3.3.7 --save
npm i typescript@3.4.5 --save-dev --save-exact
```

- [Setting Up Basic Routing and Navigation in Angular](http://www.writesomecode.in/Angular/Setting-up-basic-Routing-and-Navigation-in-Angular)
- [[routerLinkActiveOptions]="{ exact: true }"](https://medium.com/@lokeshjain2008/angular-routerlinkactive-including-fragments-8bd386ecbb2a)


```typescript
####################################################
install node
isntall angular cli
install angular material
install highcharts packages
install flex layout package

ng new myportfolio
cd myportfolio
ng add @angular/material
Choose a prebuilt theme name, or "custom" for a custom theme: Indigo/Pink
Set up HammerJS for gesture recognition? Yes
Set up browser animations for Angular Material? Yes

npm config set registry http://registry.npmjs.org/ --global
npm i highcharts-angular --save
npm i highcharts --save
npm i @angular/flex-layout @angular/cdk --save
0. Validate the setup by adding MatButtonModule and adding a button on app.component.html to see how bootstrap is working along with all the setups done so far.
=======Layout definition=========
1. Create first layout
2. Create a Component for the Dashboard page
3. Use the first layout as a Parent Route Component in app-routing.module.ts and the Dashboard page as child Component

ng g c layouts/default --skipTests false
ng g m layouts/default
ng g c modules/dashboard --skipTests false

4. Import     DefaultComponent, DashboardComponent into default.module.ts under @NgModule declarations
5. Remove DefaultComponent, DashboardComponentfrom app.module.ts and add DefaultModule in it
6. Update Routes and set to '' for Component name as DefaultComponent and append children to it as DashboardComponent in app-routing.module.ts
7. Add RouterModule to default.module.ts and <router-outlet></router-outlet> to default.component.html

You should see dashboard works! on http://localhost:4200/
=======Shared Modules definition=========
In the default.component.html add tags for header,footer and sidebar and later replace them with actuals

1. Create your Header,Sidebar and Footer components for better code organization
2. Create a Shared Module for it
3. Update the Module and add these Components in the Declaration and Exports sections.

ng g c shared/components/header --skipTests false
ng g c shared/components/sidebar --skipTests false
ng g c shared/components/footer --skipTests false
ng g m shared

4. Remove header,sidebar,footer unnecessary declaration from app.module.ts file and add them to default
5. Create component call posts under modules folder
ng g c modules/posts
6. Remove post unnecessary declaration from app.module.ts file add them to default.module.ts
7. Update children Route, for posts html page and component name as PostsComponent in app-routing.module.ts


ng g c modules/posts
ng g c modules/dept1 --skipTests false
ng g c modules/users --skipTests false
ng g c modules/users/user --skipTests false
ng g c modules/dept1/apps --skipTests false
ng g c modules/dept1/apps/edit-app --skipTests false
ng g c modules/dept1/app1/servers --skipTests false
ng g c modules/dept1/app1/servers/server --skipTests false
ng g c modules/dept1/app1/servers/edit-server --skipTests false

```
