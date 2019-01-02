# Software Engineering Markdown

This markdown file attemptsto provide many of the topics that i've covered over the last 12 years in the area of computer science. It includes links to some of my favourite articles / resources as well as some short write ups of my own interpretations of many topics / concepts that i've encountered along the way.

# HTML (Hyper Text Markup Language)

- W3C Specification https://www.w3.org/TR/html52/

## HTML5 API

TBW

# CSS (Cascasding Stylesheet)

- W3C Specifications https://www.w3.org/Style/CSS/specs.en.html

## CSS Layout

A 2018 Guide to CSS layouts https://www.smashingmagazine.com/2018/05/guide-css-layout/

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

# Fonts on the Web

TBW

# Images on the Web

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

## Shadow DOM

Custom Elements W3C Specification https://www.w3.org/TR/2018/NOTE-custom-elements-20180503/

Shadow DOM W3C Specificatin https://www.w3.org/TR/2018/NOTE-shadow-dom-20180301/

## Frameworks that use web components

Whilst these frameworks might not follow the official W3C outlines for web components they are the most popular frameworks and libraries that are recognised as using "web components" by the community today.

- Angular
- Vue.js
- React.js

# Responsive Web Applications

## Frontend Responsive Design

TBW

## Client Side Detection

### Polyfills

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

# Angular 2+

- Official Angular Documentation https://angular.io/docs
- NX (Nrwl extensions for Angular) https://nrwl.io/nx (Build out your Enterprise Angular applications for modularity and with a smarter Angular CLI. I highly recommend this).
- Angular Console https://angularconsole.com/ (GUI for the Angular CLI, good for getting further context on many commonly run commands).
- Hot Module Replacement with Angular - https://medium.com/wizardnet972/hot-module-replacement-with-angular-cli-5fc7a3ae4a9c
- Deploying Angular Applications to a serverless environment https://medium.com/@maciejtreder/angular-serverless-a713e86ea07a
- Angular Universal (Server Side Rendering) https://angular.io/guide/universal

## State Management with NgRX

TBW

# State Management for Web Applications

## Redux Design Pattern

-   Actions
-   Reducers
-   Effects

# Progressive Web Applications

## Service workers
    
## PWA Icons
 
    

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


## Deployment Environments

This can be as simple as having a development, QA, UAT and production server but there are many different configurations that can be useful depending on your project.
    
    
## Using environment variables
    
## Safely injecting and encrypting API keys
    

## Private Registries / Artefact Repositories

C# Nuget
NPM - Verdaccio
JAVA - Maven Gradle repositories.

    
#### Security on registries / artifact repositories
    
# Provisioning Tools / Virtualization / Snapshots

Chef
Vagrant
Docker / Docker Swarm
PM2
 
# Removing friction from the development workflow

Automate release notes
Avoid scope creep
Remove the need for hotfixes 

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



-   GIT Flow

- DRY Principles 
- Service-Oriented Architecture
- Microservices
    
-   Functional Programming
    
-   Reactive Programming
    
-   Separation of concerns
    
-   Modularity of Code
    
-   Unit Testing
    
-   Integration Testing
    
-   BDD with Cucumber
    
-   End to end
    
-   SOLID Principles
-   Browser Testing
-   Behavioural Testing

-   Commitzen
      
  
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
  

-   Docker
-   Docker Swarm
-   The role of clustering
-   Application clustering 
-   Server clustering
-   Application and server logging  
-   Load Balancing   
-   Message Queueing
     

# Team Management and Approaches

## LEAN Development

Link to book The LEAN Startup

## Agile Development

TBW

-   Scrum
    
-   Kanban
     

## Tools

  
-   JIRA
    
-   TeamCITY [https://www.jetbrains.com/teamcity/](https://www.jetbrains.com/teamcity/)
    
-   TFS (Microsoft Team Services)
    
 

# REST API Development

-   REST API Design Best Practices
-   JSON Web Tokens (JWT) for Authentication
-   OAuth
-   HTTP Headers
-   Swagger (Self documenting our API)
    

# JAVA Development

Spring Framework

# PHP Development

Official documentation
Composer
Laravel
Symfony
Silex

# Ruby on rails development

TBD

# C# Development

TBD

# IOS Development

TBD

# Android Development

TBD
  
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

## EOS

CLEOS
    
##  Ethereum

Web3 API
Truffle
Ganache


# Artifical Intelligence

The area of artifical technology has seen many failed and successful implementations with the goal posts being moved depending on the project. The most advanced AI that exist today are undoubtedly in the area of neural networks.

## Videos

Top 5 uses of Neural Networks (Coldfusion) https://www.youtube.com/watch?v=i9MfT_7R_4w

## Deep Learning

## Maching Learning

## Neural Networks

## Popular Libraries and Frameworks
