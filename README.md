Introducere în AngularJS
========================


Links
-----
http://act2.me/full-stack-web-development/ 
http://www.sitepoint.com/10-reasons-use-angularjs/ 
http://en.wikipedia.org/wiki/AngularJS

http://www.igvita.com/posa/high-performance-networking-in-google-chrome/ 


--------------------------

Introducere în AngularJS

--------------------------

Javascript MVC framework?

[scratch head pic here]

Cum am ajuns aici?

--------------------------

[1.png]

La inceput: give me a doc!

--------------------------

[5.png]

Give me a fragment!

Evolutia pe server-side: Scripts -> Frameworks MVC

--------------------------

[6.png]

HTML -> JSON
Dropped View

--------------------------

[8.png]

Code to assemble page (jQuery) -> Javascript MVC Framework

--------------------------
--------------------------

AngularJS - Javascript MVC framework

* two way data binding
* modules
* directives
* testing
* makes large apps maintainable

--------------------------

MVC

A lot more than Model - View - Controller

HTML enhanced for web apps!
AngularJS lets you extend HTML vocabulary for your application.

--------------------------

Two way data binding

Modificarile din model se propaga instant in view, si invers.

Model <---> View

* Mode in sync with the View.
* Scope = an object that wires up the model and view
* scope are anumite metode, like $eval

--------------------------

Modules / Servicii

Unitati care incapsuleaza o functionalitate bine definita / clase

--------------------------

Dependency Injection

* Serviciile sunt injected in controllere
* Pot fi mocked pentru testare

--------------------------

Directive

Augmenteaza codul HTML prin elemente sau atribute definite de catre developer.

Manipularea de DOM se realizeaza in interiorul directivelor, pentru a nu avea DOM manip in controllere si in tot codul.

--------------------------

Templates

{{phone.name}}
ng-repeat=””
filtre
etc.

--------------------------

Services - many built-in services

xhr, resource, route, location, 

--------------------------
--------------------------

Sendmachine - Case study

Ce are special Sendmachine?

--------------------------

ACL service + Session service

* permite accesul pe routes in functie de credentiale/grup
groups:
	* guest
	* new
	* emailconfirmed
	* confirmed
	* expired

* in caz de 401 pe orice resursa esti scos din aplicatie

--------------------------

Form Validation service

* rulează aceleași reguli atât pe front-end cat si pe back-end
* regulile folosite de backend pentru validare sunt expuse printr-un API RESTful si refolosite de catre front-end pentru validarea forms
* chained rules:
	* required | valid_email | existing_email

--------------------------

Storage + Request Cache

* stocheaza în local storage datele dintr-un form
* in cazul unui 401, 403 sa poti recupera datele introduse

--------------------------

Lang service - Localizare

* limba+locale poate fi schimbata on the fly

--------------------------

Permalink service - Deeplink

* linkuire la o anumita stare a aplicatiei

--------------------------

Chart service

* wraps Highcharts
* timeseries pe luni / zile / ore
* polling
* get: today, last_24_hours, yesterday, last_30_days

--------------------------

Directives
* pagination
* editor (ACE)
* 

--------------------------

Filters

* date (locale aware)
* numbers (locale aware)

--------------------------

