# Angular-Basics
### Angular is a javascript component based framework for building Single Page Application
### To use the Angular framework, you should be familiar with 

* JavaScript
* HTML
* CSS

### To install angular on your system, you must have node.js  and  npm
### npm  is installed with node.js by default

### Angular, the Angular CLI, and Angular applications depend on npm package manager to download and install npm packages.

### Angular CLI can be used to create,test, bundle, and deploy applications.

### To install the Angular CLI on a terminal,type the command:

```bash
npm install -g @angular/cli
```
### To create a new angular application,type the CLI command on the terminal
```bash
ng new appName
```
### To run your new application, navigate to the app folder,then serve  it. This automatically opens your browser to http://localhost:4200/.

```bash
cd appName
ng serve --o

```
### The ng serve command opens the server, watches and  rebuilds your application as you make changes to it.
### Angular is written in Typescript and interpreted to javascript during  code execution

###  An angular application is made up of components, which  are the main building blocks for Angular applications.
### A component consists of:
* An HTML template that  serves as the view that gets rendered to the browser, and has some syntax that enables it communicate with the typescript clas
* A Typescript class that contains the logic
* A CSS selector that defines how the component is used in a template

### App component is the main component of every angular application, which is rendered in the index.html file 
 ```bash
 <app-root><\app-root>
 ```
 ### If removed from the index.html file, nothing gets rendered to the browser
### The typescript file can contain styles and HTML, but is better to use components when there are several lines of code.
```bash
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `
    <h2>App Component</h2>
    <p>This is the main component, where other components are rendered!</p>
  `
  styles:[`h2{color:red;
  font-size:12px;
  }`]
})
export class AppComponent {
  // The contains the methods and properties.
}
```
 ### To create a component in Angular,you can use the terminal or do it manually
```bash
ng generate c <componentName>, where <componentName> is the name of your component
```
###  This command creates the following by default:
 * A directory named after the component
 * A component file, <componentName>.component.ts
 * A template file, <componentName>.component.html
 * A CSS file, <componentName>.component.css
 * A testing specification file, <componentName>.component.spec.ts
 
### Values of properties in the component class, can be rendered in the HTML template dynamically, using curly braces

```bash
import { Component } from '@angular/core';

@Component ({
  selector: 'app-root',
  templateUrl: './app.component.html'
})
export class AppComponent {
    message = 'This value gets rendered in the HTML, using {{}}';
}
```
```bash
<p>{{ message }}</p>
```
