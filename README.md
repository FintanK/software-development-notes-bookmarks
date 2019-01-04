# :books: :ledger: Software Development Notes and Bookmarks

This markdown file (which is most certainly a work in progress right now ) attempts to help me revise many of the topics that i've covered over the last 12 years in the area of computer science. It includes links to some of my favourite articles / resources as well as some short write ups of my own interpretations of many topics / concepts that i've encountered along the way.

# Some of my favourite websites

https://github.com/dypsilon/frontend-dev-bookmarks - Frontend development bookmarks
https://developer.mozilla.org/en-US/docs/Web - Mozilla Developer Network
http://www.tutorialspoint.com/ - Tutorialspoint
https://www.smashingmagazine.com/ - Smashing Magazine
https://tympanus.net/codrops/ - Tympanus Codrops
https://www.toptal.com/developers/blog - Toptal

# Developer Blogs

https://flaviocopes.com/ - Flavio Copes (Frontend development).
https://toddmotto.com/ - Todd Motto (Angular).
https://johnpapa.net/ - John Papa
https://angular-university.io/my-courses - Angular University

# Markdown

Markdown reference https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

# HTML (Hyper-Text Markup Language)

- W3C Specification https://www.w3.org/TR/html52/

## HTML5 API

HTML 5 API Overview (Handy reference) https://platform.html5.org/

# CSS (Cascasding Stylesheet)

- W3C Specifications https://www.w3.org/Style/CSS/specs.en.html

## CSS Layout

A 2018 Guide to CSS layouts https://www.smashingmagazine.com/2018/05/guide-css-layout/
Browser Media Queries https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries

## Popular CSS Libraries and Frameworks

Bootstrap https://getbootstrap.com/docs/4.0/getting-started/introduction/
Foundation https://foundation.zurb.com/
Bulma https://bulma.io/
UIkit https://getuikit.com/
Semantic UI https://semantic-ui.com/

## CSS Preprocessors

- SASS
- LESS

## CSS Coding Standards

- BEM (Block Element Modifier) http://getbem.com/introduction/

# XML (Extensible Markup Language)

Extensible Markup Language is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. The W3C's XML 1.0 Specification and several other related specifications—all of them free open standards—define XML

A list of popular XML Schemas used on the web https://en.wikipedia.org/wiki/List_of_types_of_XML_schemas

# Fonts on the Web

Web Fonts Guide https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts

# Images on the Web

TBW

## Image Optimization

## Responsive Images

# Bandwidth Optimization for Web Applications

TBW

# State Management for Web Applications

Just like the server, the browser can have different types of states to manage...

- Server Response Data
- User information
- User Input
- UI State
- Router / location state

State Management Libraries

- Model our app state
- Update the state
- Read state values
- Monitor changs to the state

## The Redux Design Pattern / Architecture

The three principles of Redux.

- Single source of truth.
- State is read-only.
- Pure functions update the state

One of the biggest benefits of using state management is that the duplicate dependency injection of data services
can be moved out from the components to the state management library implementation.

In Universal (Server side rendered) Angular apps you can prepopulate the store on page load and avoid the many HTTP many requests needed for this logic with an SPA (Single Page Application).

Great developer tools including time travel debugging.

Easier testing of how data retrieved in the client application is used.

Because the state is read only, our components just have to **react** to state changes. Our components role when using state management is to subscribe to the store and respond appropriately.

#### Redux Core Concepts

###### Single state tree

A single state tree is a single Javascript object. It is composed / built up using reducers.

It has an initial state. When the application loads.

**An example state**

```
const state = {
    todos: []
};
```

###### Actions

Actions have two properties

- Type (usually a string, describing the action).
- Payload (this is optional)

These are dispatched by components in order to update the application state but do not update the state themselves. This gives us an "immutable update pattern" which basically means that we clearly define how data is updated in our client applications.

```
const action = {
    type: 'ADD_TO_DO',
    payload: {
      label: 'Go for a jog',
      complete: false
    }
};
```

###### Reducers

These are pure functions (taken from the functional programming methodology) that update the application state. Given the same input they will always have the same output. They don't modify any data outside of their functional scope. This output is typically an updated application state.

This is a pure function. It does not mutate any data outside of it's own scope.

```
function reducer(state, action) {
    switch(action.type) {
       case: 'ADD_TO_DO': {
        const todo = action.payload;
        const todos = [...state.todos, todo],
        return [ todos]; // Update the state and pass back
       }
    }  
    return state; // Return the passed state by default
}
```

This would result in the state being updated

```
const state = {
    todos: [
      { labelL 'Go for a jog', complete: false }
    ]
};
```

###### Store

- The state container. Injected into components that need it.
- Components use the store to dispatch events
- Components use the store to subscribe to state updates.
- Handles responsibility of invoking reducers.

###### One-way data flow.

![One way data flow in redux](http://www.mrscottmcallister.com/assets/img/redux-flow.png)

###### Immutability

"An immutable object is an object that cannot be modified after creation."

Why would we make an object immutable?

- Predictability
- Explicit State Changes
- Performance
- Mutation Tracking
- Undoing state changes

# Semantic Web Applications

The first reference to the term "Semantic Web" was made by Tim Berners Lee back in 2011 in this publication [Google Scholar Link](http://scholar.google.co.uk/scholar_url?url=https://kask.eti.pg.gda.pl/redmine/projects/sova/repository/revisions/master/entry/doc/Master%2520Thesis%2520(In%2520Polish)/materials/10.1.1.115.9584.pdf&hl=en&sa=X&scisig=AAGBfm2r1XqP0ka20GZUp7W6sZup22to4Q&nossl=1&oi=scholarr)

Wikipedia Article https://en.wikipedia.org/wiki/Semantic_Web

**Personal Opinion**: I studied this topic as part of my university thesis. I personally believe that the outlined solutions proposed by the W3C however interesting will not be accomodated any time soon by the majority of websites. Because of the flexible nature of HTML, CSS and Javascript coding practices websites will not provide structured markup required for the interopability of websites in this manner. 

Content Management Systems,oding Frameworks by be able to incorporate these coding practices in the future and take the manual work of adding context to markup out of the developers workflow.

#### HTML Ontologies / Schemas

FOAF (Friend of a friend) http://xmlns.com/foaf/spec/
Open Graph Protocol http://ogp.me/ (Facebook uses this for links)
W3C Spec on HTML Microdata https://www.w3.org/TR/microdata/
RDFa (RDFa is an extension to HTML5 that helps you markup things like People, Places, Events, Recipes and Reviews. Search Engines and Web Services use this markup to generate better search listings and give you better visibility on the Web, so that people can find your website more easily) https://rdfa.info/

#### Javascript Ontologies / Schemas

JSON LD (JSON Linked Data) https://json-ld.org/

# Web Components

An introduction to web components from Mozilla https://developer.mozilla.org/en-US/docs/Web/Web_Components
Custom Elements W3C Specification https://www.w3.org/TR/2018/NOTE-custom-elements-20180503/

## Shadow DOM

Shadow DOM refers to the ability of the browser to include a subtree of DOM elements into the rendering of a document, but not into the main document DOM tree.

Shadow DOM W3C Specificatin https://www.w3.org/TR/2018/NOTE-shadow-dom-20180301/

## Frameworks that use web components

Whilst these frameworks might not follow the official W3C outlines for web components they are the most popular frameworks and libraries that are recognised as using "web components" by the community today.

- Angular
- Vue.js
- React.js

# Responsive Web Applications

## Frontend Responsive Design

Media Queries

## Client Side Detection

#### Browser User Agent

- Check your browser user agent https://www.whatismybrowser.com/detect/what-is-my-user-agent
- Mozilla Developer Network - Browser detection using the user agent https://developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent

#### Polyfills

Polyfills allow older browsers to handle HTML, CSS and Javascript features that would typically not be available with your client side code.
    
## Server Side Detection

Server side detection is a very powerful technique that allows you to detect the users device, browser and browser capabilities before serving any content to their device. This allows you to customize the user experience and cater to any progresive functionality that their device and browser may support.

- Using supported HTML5 API
- Hardware capabilities
- Supported network protocols
- Video, audio
- JAVA
- Optimize the bandwidth used for the website when serving HTML, CSS, Javascript, Images, Fonts etc.

#### Server Side Detection Solutions

DeviceAtlas https://deviceatlas.com/
Wurfl - http://wurfl.sourceforge.net/
Scientamobile - https://www.scientiamobile.com/

# IDE (Integrated Development Environments)

-   VSCode
-   WebStorm
-   IntelliJ IDEA

# Web Servers

## Apache

TBW

## Nginx

TBW

## IIS

TBW

# Node.js

- Package Managers (NPM, YARN)
- Open Source Packages https://www.npmjs.com/
- Set up your own private registry https://github.com/verdaccio/verdaccio
- Exporting Modules https://flaviocopes.com/node-export-module/
- Node.js - Why use it? https://thinkmobiles.com/blog/why-use-nodejs/
- Non-blocking IO / Event Loop / nextTick function
- Asynch await
- Streams - https://flaviocopes.com/nodejs-streams/
- Websockets - https://flaviocopes.com/node-websockets/
- Linting - ESLint - https://eslint.org/
- Babel Transpiler https://babeljs.io/ - (Node.js uses ES5, Use ES6 for your app!).
- Semantic Versioning https://flaviocopes.com/npm-semantic-versioning/
- Package-lock.json - https://flaviocopes.com/package-lock-json/
- Functional programming: https://medium.freecodecamp.org/an-introduction-to-functional-programming-style-in-javascript-71fcc050f064 (Pure, impure functions)

Much more to come here.

## Popular Node.js Packages and Libraries

#### Express.js

The most popular Node.js module for creating REST API https://expressjs.com/

#### Helmet.js

This allows you to secure your REST API by locking down the used headers https://github.com/helmetjs/helmet

#### RxJS  

Creating and Subscribing to Observables with RXJS. [Click here](https://coursetro.com/posts/code/148/RxJS-Observables-Tutorial---Creating-&-Subscribing-to-Observables)

Subjects (BehaviourSubject, ReplaySubject, Asynch) with RXJS. [Click here](https://coursetro.com/posts/code/149/RxJS-Subjects-Tutorial---Subjects,-BehaviorSubject,-ReplaySubject-&-AsyncSubject)
  
Operators with RXJS [Click here](https://coursetro.com/posts/code/150/RxJS-Operators-Tutorial---Learn-How-to-Transform-Observables)

#### Axios 

https://github.com/axios/axios - Promise based HTTP client for the browser and node.js

#### Lodash
    
Utility library for many common Javascript use cases https://lodash.com/

#### MomentJS

https://momentjs.com/docs/ - Official docs.
https://momentjs.com/timezone/ - Moment Timezone.

#### IPFS

Distributed file system that seeks to connect all computing devices with the same system of files https://ipfs.io/

#### Ramda

Purely functional Javascript utility Library

https://github.com/ramda/ramda

Much more to come!

# Typescript

- Official Handbook https://www.typescriptlang.org/docs/handbook/basic-types.html
- DefinitelyTyped (The repository for high quality) https://github.com/DefinitelyTyped/DefinitelyTyped
- https://www.npmjs.com/package/swagger-ts-generator

## Popular Typescript Libraries and Generators

- https://www.npmjs.com/package/swagger-ts-generator (Generate Types from your swagger documentation)

## Linting

TSLint https://palantir.github.io/tslint/
TSLint formatters https://palantir.github.io/tslint/formatters/
AirBNB TSLint (Just extend this in your TSLint configuration to use it in your project, you can override and customize these settings) https://www.npmjs.com/package/tslint-config-airbnb

# Angular

- Official Angular Documentation https://angular.io/docs
- NX (Nrwl extensions for Angular) https://nrwl.io/nx (Build out your Enterprise Angular applications for modularity and with a smarter Angular CLI. I highly recommend this).
- Angular Console https://angularconsole.com/ (GUI for the Angular CLI, good for getting further context on many commonly run commands).
- Hot Module Replacement with Angular - https://medium.com/wizardnet972/hot-module-replacement-with-angular-cli-5fc7a3ae4a9c
- Deploying Angular Applications to a serverless environment https://medium.com/@maciejtreder/angular-serverless-a713e86ea07a
- Angular Universal (Server Side Rendering) https://angular.io/guide/universal

## Learning resources

https://ultimatecourses.com/angular - My most recommended course.
https://www.tutorialspoint.com/angular6 - A useful overview of coure Angular concepts.

## Other concepts

Angular Interceptors

more to come here..

## Useful Angular Packages

- https://github.com/atularen/ngx-monaco-editor (Browser-based code editor for Microsoft. Angular component.)

## Architecting your Angular applications with Nx (Highly recommended)

Nx is brilliant. It allows you to manage your application with a more advanced CLI tool that automates more than the standard Angular CLI.

Nx Workspace
Workspace-Specific Schematics
State Management
NgRx
Data Persistence
Linters
Code Formatter
UpgradeModule and dowgradeModule helpers

Find out more at https://nrwl.io/nx/overview

## State Management with NgRX for Angular.

NgRX at it's core is made up of NgRX Store and Effects. It utilizes the popular Rx.js library and it's observable design pattern to
provide a Redux architecture for state management in Angular.

NgRX Store on Github https://github.com/ngrx/store
NgRx Effects https://github.com/ngrx/effects

There are other libraries than can be used with NgRX but they are optional.

#### What is NgRX Store?

Official documentation https://ngrx.io/guide/store

Inspired by the Redux architecture NgRX Store using RXJS Observables to provide state management in Angular.

###### Benefits of NgRX Store

- Single source of truth
- Testability
- Performance Benefits (one-way data flow. No unexpected events in your components around data management).
- Root and feature module support (eager ad laxy loaded modules).

###### Store selectors

This is probably the toughest part about NgRX in general but they are well worth implementing

A very basic component implementation interacting with the store would look something like this..

```
import { Store } from '@ngrx/store'
// other imports

export class YourCustomComponent implements OnInit {

   constructor(private store: Store<fromStore.ToDosState>) {
    
   }
   
   ngOnInit() {
    this.store.select<>('todos').subscribe() // etc
   }

};

```

You can however define functions in your store that care of all of the logic for navigating the state and getting the data your are looking for. These can be imported and used to select data specifically from your store. Your component can then store the observables and use asynch in your components to handle changes to the state reactively.

You can use a naming convention for observables that are stored on your component. Typically using the $ at the end of the variables name is a good idea.

```
import { Store } from '@ngrx/store'
// other imports

export class YourCustomComponent implements OnInit {

   todos$: Observable<ToDo[]>

   constructor(private store: Store<fromStore.ToDosState>) {
    
   }
   
   ngOnInit() {
    this.todos$ = this.store.select>(fromStore.getAllToDos)
   }

};

```

Then in your HTML for the component

```
<div *ngIf="!((todos$ | asynch)?.length)">
    These are currently no to do items
</div>
<to-do-item *ngFor="let todo of (todos$ | asynch)" [todo]="todo"></to-do-item>
```

This observables and asynch approach makes your components implement a reactive architecture.

#### What are NgRX Effects?

Official doccuentation https://ngrx.io/guide/effects

- Listen for ngrx/store actions that are dispatched
- Isolate side effects from components
- Communicate outside of Angular (Handle API calls, websockets etc)

![NgRX Effects Flow](https://cdn-images-1.medium.com/max/1600/1*vSadxKWVoAirhVCa8fxiNw.png)

Because reducers are pure functions these are not ideal places to put API calls

If an effect fetches data from an external source then it will dispatch an action of it's own with a reducer handling it and updating the state

Effects don't perform service calls themselves. They will typically offload that work to an Angular service.

###### Optimizing data structures with Entities

In our reducers we can make how we index our data more efficient so that we can use our redux dev tools to easily view and navigate our state

#### Redux Dev Tools - Highly recommended

This will allow you see every single action and state change in your app. 

It really showcases how reactive your application is when built using the redux pattern.

You can also step back in time to an older state to debug issues with your application by dragging the slider.

It will also visualize your state tree in an easy to understand way if you index your data with the entities approach outlined above.

You can download the extension here http://extension.remotedev.io/

#### Setting up NgRX Router Store

This allows us to integrate our router state to the redux store in our application which is quite useful for even more debugging with
our dev tools. It also makes our application more reactive.

TBW

** I will be providing a link here to my own reference Angular application with state management **

#### My own lessons from implementing state management with NgRX

- State Management with Angular requires a lot of extra code. This can be generated automatically though with the CLI once NgRX schematics have been added to your project https://ngrx.io/guide/schematics . It's even better using NX https://nrwl.io/nx/guide-setting-up-ngrx
- Implement container components for each feature (these are basically the top most parent components for each module).
- Hook up your router to the state
- Make both your routing and store actions resource based (from the API down to the store for consistency, bespoke functionality can be implemented at the component level).
- Keep your stores inside of the relevant modules only. This will allow you to keep your feature implementations modular.
- Optimize your folder structure with index.ts files wherever possible to avoid too many imports.

## Angular Module / Folder Organisation Best Practices

## Angular Unit Testing

JEST
KARMA

## Angular End to End Testing

BDD
Cucumber
Protractor

# Progressive Web Applications

## Service workers

TBW
    
## PWA Icons
 
TBW   

# Build Tools for Web Applications

The role of a build tool in web applications is take the source development assets for your application and produce optimized assets that
will be used to run your application.

This can include tasks such as

- Copy, deleting files
- Merging files
- Compiling code
- Optimizing code 
- Removing spaces
- Producing index files
- Optimizing images, fonts other assets.
- Any other tasks you wish to automate with your application setup.

## Grunt

Javascript Task runner with an impressive list of plugins https://gruntjs.com/

## Gulp

Another Javascript build tool for automating common tasks https://gulpjs.com/

## Webpack

Angular uses webpack.

# Browser Build Optimization
    
- Semantic browser applications: Schema generation.
- Optimizing Images (PNG, SVG,)
- Optimizing fonts
- Minification of files
- Concatenation of files

# Progressive Browser Functionality

- WEBRTC https://webrtc.org/
- Web Assembly https://webassembly.org/
- WebGL https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Tutorial/Getting_started_with_WebGL
 
## Native application development using Web Technologies

#### Cordova 

Develop applications for native operating systems with HTML, CSS and Javascript https://cordova.apache.org/
  
#### Electron
 
Develop desktop applications with HTML, CSS and Javascript https://electronjs.org/

#### Ionic Native

- Nativescript  

#### NW.js (Previously node-webkit)

Lets you call all Node.js modules directly from DOM and enables a new way of writing applications with all Web technologies.

https://nwjs.io/

# Version Control

## Mercurial

## SVN (Subversion)

## GIT - Now the most popular

How merkle trees work https://en.wikipedia.org/wiki/Merkle_tree

# Continuous Deployment / Integration for Teams

## Cloud Services

#### Microsoft Azure

https://azure.microsoft.com/en-gb/services/ - Overview of products and solutions

#### Google Cloud Services

https://cloud.google.com/products/ - Overview of products and solutions

## Deployment Environments

This can be as simple as having a development, QA, UAT and production server but there are many different configurations that can be useful depending on your project.
    
## Environment variables: Why and how.


    
## Safely injecting and encrypting API keys
    
TBW

## Private Registries / Artefact Repositories

Verdaccio (NPM Registry)
JAVA - Maven Gradle repositories.

## CI Platforms and Tools

https://semaphoreci.com/ - Semaphore CI
https://jenkins.io/ - Jenkins
https://azure.microsoft.com/en-gb/solutions/architecture/azure-devops-continuous-integration-and-continuous-deployment-for-azure-web-apps/ - Microsoft Azure CI/CD
https://cloud.google.com/cloud-build/ - Google Cloud Build
https://aws.amazon.com/ - Amazon Web Services

## IAAS (Infrastructure as a service)

https://www.netlify.com/ - All-in-one platform for automating modern web projects.

#### Security on registries / artifact repositories
    
# Provisioning Tools / Virtualization / Snapshots

## Chef

TBW

## Vagrant

## Docker 

#### Docker Swarm

## PM2

TBW
 
# Removing friction from the development workflow

## Automate release notes

TBW

## Avoiding scope creep


## Removing the need for hotfixes 

TBW

# Software Development and Testing Strategies

## Principles of Software Engineering

Rigor and formality
Separation of concerns
Modularity and decomposition
Abstraction
Anticipation of change
Generality
Incremental Development
Reliability

## Software Engineering Concepts

#### Flux Architecture

https://facebook.github.io/flux/docs/overview.html#content - Flux Architecture

#### DRY Principles 

#### Service-Oriented Architecture

#### Microservices

#### Functional Programming 

#### Reactive Programming

#### Separation of concerns

#### Modularity of Code 

#### Unit Testing

#### Code Coverage

#### Integration Testing

#### BDD (Behaviour driven development)

#### End to end testing

#### SOLID Principles

#### Cross Browser Testing
      
  
# Databases

## Concepts

## MySQL

## SQL Server

## Postgres

## MongoDB

## Redis

## Cassandra

## CouchDB


# Distributed Computing

# Logging

TBW
  

# Release Management

-   GIT Branching Strategies 
-   Automated and Semantic Versioning
 
# Coding Standards

- Google HTML and CSS Code Standards https://google.github.io/styleguide/htmlcssguide.htmlRDFa is an extension to HTML5 that helps you markup things like People, Places, Events, Recipes and Reviews. Search Engines and Web Services use this markup to generate better search listings and give you better visibility on the Web, so that people can find your website more easily.

# Scaling applications for Enterprise use and large traffic
  
-   Docker https://www.docker.com/
-   Docker Desktop https://www.docker.com/products/docker-desktop
-   Docker Hub https://hub.docker.com/
-   Kitematic (Simple to use GUI tool to provision docker containers on your desktop). https://kitematic.com/
-   Docker Swarm
-   Kubernetes https://kubernetes.io/
-   The role of clustering
-   Application clustering 
-   Server clustering
-   Application and server logging  
-   Load Balancing   
-   Message Queueing   

# IT Law

PCI ( Payment Card Industry) Compliance https://www.pcicomplianceguide.org/faq/

## Software Licenses

Software license guide https://choosealicense.com/licenses/

# Team Management and Approaches

## Agile Development

#### Scrum

Scrum.org Guide https://www.scrumguides.org/scrum-guide.html
Scrum at Scale Guide https://www.scrumatscale.com/scrum-at-scale-guide-read-online/

Product Owner Role https://www.mountaingoatsoftware.com/agile/scrum/roles/product-owner
Scrum Master Role https://www.mountaingoatsoftware.com/agile/scrum/roles/scrummaster
Scrum Team Role https://www.mountaingoatsoftware.com/agile/scrum/roles/team    
    
#### Kanban and LEAN Development

Principles of LEAN Development https://leankit.com/learn/lean/principles-of-lean-development/

#### Books

The LEAN Startup by Eric Ries http://theleanstartup.com/

https://www.blueprintsys.com/agile-development-101/agile-methodologies - A guide to Agile Methodologies

#### XP (Extreme Programming)
     

#### Tools
 
- JIRA  https://www.atlassian.com/software/jira
- JIRA Ops https://www.atlassian.com/software/jira/ops
- Confluence https://www.atlassian.com/software/confluence
- TeamCITY [https://www.jetbrains.com/teamcity/](https://www.jetbrains.com/teamcity/) 
- TFS (Microsoft Team Services) (Now Azure Devops Server) https://azure.microsoft.com/en-us/services/devops/server/
- Lists, boards and cards https://trello.com/
 
# Protocol

## HTTP

# REST API Development

## REST API Design Best Practices

## Authentication

#### JSON Web Tokens (JWT) for Authentication

TBW

#### OAuth

TBW

## Documentation

Swagger (Self documenting your API) https://swagger.io/
    
# JAVA Development

JAVA Spring Framework https://spring.io/
Pivotal Cloud Foundry (Manage your project, develop, builkd test deploy) https://pivotal.io/platform , https://pivotal.io/learn

# PHP Development

Awesome PHP https://github.com/ziadoz/awesome-php (Comprehensive .NET Development Bookmarks)

Official documentation http://php.net/manual/en/
Composer (The best PHP package manager for dependency management) https://getcomposer.org/
Laravel (One of the best PHP Frameworks) - https://laravel.com/
Symfony (Also one of the best PHP Frameworks) - https://symfony.com/
Silex - Lightweight PHP Framework https://silex.symfony.com/
Wordpress Codex - Build your applications on top of wordpress with custom themes, plugins etc - https://codex.wordpress.org/

# Ruby on rails development

Official documentation https://guides.rubyonrails.org/

# C# Development

Awesome .NET https://github.com/quozd/awesome-dotnet (Comprehensive .NET Development Bookmarks)

NuGet package manager https://www.nuget.org/
.NET Entity Framework https://docs.microsoft.com/en-us/ef/
Azure devops (Will succeed Nuget private servers) https://azure.microsoft.com/en-gb/services/devops/
  
# Blockchain Development

The blockchain is a promising technology that has progressed at an ever increasing rate. It is now used in most industries to improve trust and transparency as well as provide an immutable record of distributed data. Many people have heard of bitcoin but distributed ledger technology provides potentially more valuable technologies.

- Peer to peer cash (Everyone becomes their own bank)
- Programmable money and universal cash without government inflation.
- Automated brokering
- Removal of third party intermediaries
- Distributed organisations with no central control
- Truly consensus based platform
- Uncensorable data

# Videos

How blockchain is alredy taking over (Coldfusion) https://www.youtube.com/watch?v=kP6EezXJKNM
How big is Bitcoin? https://www.youtube.com/watch?v=zrY3i85W5tU

## Bitcoin

Bitcoin whitepaper https://bitcoin.org/bitcoin.pdf

## EOS

EOS Developers Portal https://developers.eos.io/
    
##  Ethereum

Web3 API https://github.com/ethereum/wiki/wiki/JavaScript-API

#### Popular Ethereum Tools and Libraries

Truffle https://github.com/trufflesuite/truffle
Ganache https://truffleframework.com/ganache

## Interesting Blockchain Projects

https://storj.io/ - Distributed data storage with clients earning tokens for the storage they provide.


