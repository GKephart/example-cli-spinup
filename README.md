# example-cli-spinup
a quick demo on how to add angular to an existing Capstone porject.

### Initial setup 
The initial setup can be done by only one capstone member but I reccomend everyone work together.

 1. update the `/.gitignore` file
 ```
*/dist
*/tmp
*/out-tsc
/node_modules
.project
.classpath
.c9/
*.launch
.settings/
*.sublime-workspace
/.sass-cache
/connect.lock
/coverage
/libpeerconnection.log
npm-debug.log
testem.log
/typings
/e2e/*.js
/e2e/*.map
Thumbs.db
 ```
 
 2. install angular-cli `sudo npm install -g @angular/cli`
 3. cd into the project and run `ng new --create-application --minimal --skip-git`
 answers to the prompt from the ng command
  * ? What name would you like to use for the new workspace and initial project : ng
  * ? Would you like to add Angular routing? (y/N) : N
  * ❯ CSS    (.css ) : select CSS
 4. commit and push the changes propagated by running the `ng` command
 5. add `app.routes.module.ts` to `/ng/src/app`
 6. replace `/ng/src/app/app.module` with the app.module.ts in https://bootcamp-coders.cnm.edu/class-materials/angular2/introduction/
 7. add the packages below to the dependencies object in `/ng/package.json`
 ```
 "@ng-bootstrap/ng-bootstrap": "^4.0^",
 "@auth0/angular-jwt": "2.0^",
 "ngx-cookie":"4.1.2^"
 ```
 8. add the packages below to the dev dependencies object in `ng/package.json`
 ```
  "@fortawesome/fontawesome": "^1.1.7",
  "@fortawesome/fontawesome-free-brands": "^5.0.12",
  "@fortawesome/fontawesome-free-regular": "^5.0.12",
  "@fortawesome/fontawesome-free-solid": "^5.0.12",
 ```
 9. add `@import url('https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css');` to `/ng/src/styles.css`
 10. delete the template in @component at `/ng/src/app/app.component.ts`
 11. create `/ng/src/app/app.component.html` and add `<router-outlet></router-outlet>` to the template.
 12. add the new app.component.html to the @component decorator in `/ng/src/app.component.ts` 
```
@ngComponent({
selector: 'my-app',
  templateUrl: './app.component.html',
})
```
13. create a generic splash component with a template
* make sure to create both a `/ng/src/app/splash/splash.component.ts` and make sure to create both a `/ng/src/app/splash/splash.component.html` feel free to copy code from this repository`
14. 
 

 
 
  
  
 
  
 
